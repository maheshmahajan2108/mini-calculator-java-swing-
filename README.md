# mini-calculator-java-swing-
mini calculator using java swing 
//LogInForm 
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

class Myframe extends JFrame implements ActionListener{
	private Container c;
	private JLabel l1,l2, result;
	private JTextField t1,t2;
	private JButton add,sub,mul,div;
	Myframe(){
		setTitle("Calculater example by MM");
		setSize(300,300);
		setLocation(100,100);
		setLayout(null);
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		c=getContentPane();
		
		l1=new JLabel("first number");
		l1.setBounds(10,20,100,20);
		c.add(l1);
		
		t1=new JTextField();
		t1.setBounds(120,20,100,20);
		c.add(t1);
		
		
		l2=new JLabel("second number");
		l2.setBounds(10,50,100,20);
		c.add(l2);
		
		t2=new JTextField();
		t2.setBounds(120,50,100,20);
		c.add(t2);
		
		add=new JButton("+");
		add.setBounds(10,80,50,30);
		c.add(add);
		
		sub=new JButton("-");
		sub.setBounds(70,80,50,30);
		c.add(sub);
		
		mul=new JButton("*");
		mul.setBounds(130,80,50,30);
		c.add(mul);
		
		div=new JButton("/");
		div.setBounds(180,80,50,30);
		c.add(div);
		
		result=new JLabel("result :");
		result.setBounds(10,120,150,20);
		c.add(result);
		
		add.addActionListener(this);
		sub.addActionListener(this);
		mul.addActionListener(this);
		div.addActionListener(this);
		setVisible(true);
	}
	public void actionPerformed(ActionEvent e){
		if(e.getSource()==add){
			int a=Integer.parseInt(t1.getText());
			int b=Integer.parseInt(t2.getText());
			int c=a+b;
			result.setText("result:"+c);
		}
		if(e.getSource()==sub){
			int a=Integer.parseInt(t1.getText());
			int b=Integer.parseInt(t2.getText());
			int c=a-b;
			result.setText("result:"+c);
		}
		if(e.getSource()==mul){
			int a=Integer.parseInt(t1.getText());
			int b=Integer.parseInt(t2.getText());
			int c=a*b;
			result.setText("result:"+c);
		}
		if(e.getSource()==div){
			int a=Integer.parseInt(t1.getText());
			int b=Integer.parseInt(t2.getText());
			int c=a/b;
			result.setText("result:"+c);
		}
	}
}
class Simplecalsi{
	public static void main(String arg[])
	{
		Myframe frame=new Myframe();
	}
}
