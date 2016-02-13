//# JFrame-Test
import javax.awt.*;
import java.swing.*;
public class Test extends JFrame
{
   public Test()
   {
      super("Frame Test");
      setSize(145, 145);
      setLookAndFeel();
      setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
      JButton one = new JButton("One");
      JButton two = new JButton("Dos");
      JButton three = new JButton("San");
      JPanel pane = new JPanel();
      pane.add(one);
      pane.add(two);
      pane.add(three);
      add(pane);
      setVisible(true);
   }
   
   private static void setLookAndFeel()
   {
      try
      {
         UIManager.setLookAndFeel("com.sun.java.swing.plaf.nimbus.NimbusLookAndFeel");
         SwingUtilities.updateComponentTreeUI(this);
      }
      catch (Exception e)
      {
         System.err.println("Couldn't use the system look and feel: " + e);
      }
   }
   
   public static void main(String[] args)
   {
      Test() buttons = new Test();
   }
}
