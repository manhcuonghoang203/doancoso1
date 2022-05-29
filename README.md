import java.awt.BorderLayout;
import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JPanel;
import javax.swing.border.EmptyBorder;
import javax.swing.JButton;
import java.awt.event.ActionListener;
import java.beans.Visibility;
import java.awt.event.ActionEvent;
import javax.swing.JTextField;

public class Client extends JFrame implements ActionListener {

	
	private JPanel contentPane;
	
	private JButton visibleAddNote;
	private JButton addNote;
	
	int dem=0;
	
	private JButton del1;
	private JButton del2;
	private JButton del3;
	private JButton del4;
	private JButton del5;
	
	private JTextField TF1;
	private JTextField TF2;
	private JTextField TF3;
	private JTextField TF4;
	private JTextField TF5;
	

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Client frame = new Client();
					frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the frame.
	 */
	public Client() {
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(70, 10, 1800, 1000);
		contentPane = new JPanel();
		contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
		setContentPane(contentPane);
		contentPane.setLayout(null);
		
		visibleAddNote = new JButton("Are you have work?");

		visibleAddNote.setBounds(0, 0, 302, 120);
		contentPane.add(visibleAddNote);
		
		addNote = new JButton("ADD");
		addNote.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
			}
		});
		addNote.setVisible(false);
	
		addNote.setBounds(0, 117, 150, 168);
		contentPane.add(addNote);
		
		TF1 = new JTextField();
		TF1.setBounds(160, 131, 302, 32);
		contentPane.add(TF1);
		TF1.setColumns(10);
		TF1.setVisible(false);
		
		
		TF2 = new JTextField();
		TF2.setColumns(10);
		TF2.setBounds(160, 174, 302, 32);
		contentPane.add(TF2);
		TF2.setVisible(false);
		
		
		TF3 = new JTextField();
		TF3.setColumns(10);
		TF3.setBounds(160, 217, 302, 32);
		contentPane.add(TF3);
		TF3.setVisible(false);
		
		TF4 = new JTextField();
		TF4.setColumns(10);
		TF4.setBounds(160, 260, 302, 32);
		contentPane.add(TF4);
		TF4.setVisible(false);
		
		TF5 = new JTextField();
		TF5.setColumns(10);
		TF5.setBounds(160, 303, 302, 32);
		contentPane.add(TF5);
		TF5.setVisible(false);
		
		del1 = new JButton("X");
		del1.setBounds(483, 131, 44, 32);
		contentPane.add(del1);
		del1.setVisible(false);
		
		del2 = new JButton("X");
		del2.setBounds(483, 174, 44, 32);
		contentPane.add(del2);
		del2.setVisible(false);
		
		del3 = new JButton("X");
		del3.setBounds(483, 217, 44, 32);
		contentPane.add(del3);
		del3.setVisible(false);
		
		del4 = new JButton("X");
		del4.setBounds(483, 260, 44, 32);
		contentPane.add(del4);
		del4.setVisible(false);
		
		
		del5 = new JButton("X");
		del5.setBounds(483, 303, 44, 32);
		contentPane.add(del5);
		
		JButton playMusic = new JButton("play");
		playMusic.setBounds(-11, 874, 191, 98);
		contentPane.add(playMusic);
		
		JButton nextMusic = new JButton("next");
		nextMusic.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
			}
		});
		nextMusic.setBounds(178, 892, 191, 58);
		contentPane.add(nextMusic);
		
		JButton visible = new JButton("acs");
		visible.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
			}
		});
		visible.setBounds(1740, 693, 44, 120);
		contentPane.add(visible);
		
		JButton btnNewButton_1 = new JButton("New button");
		btnNewButton_1.setBounds(1695, 627, 89, 54);
		contentPane.add(btnNewButton_1);
		
		JButton btnNewButton_2 = new JButton("New button");
		btnNewButton_2.setBounds(1641, 693, 89, 54);
		contentPane.add(btnNewButton_2);
		
		JButton btnNewButton_3 = new JButton("New button");
		btnNewButton_3.setBounds(1641, 759, 89, 54);
		contentPane.add(btnNewButton_3);
		
		JButton btnNewButton_4 = new JButton("New button");
		btnNewButton_4.setBounds(1695, 824, 89, 54);
		contentPane.add(btnNewButton_4);
		del5.setVisible(false);
		
		addAction();
	   
		
	}
	
	private void addAction(){
        visibleAddNote.addActionListener(this);
        addNote.addActionListener(this);
        del1.addActionListener(this);
        del2.addActionListener(this);
        del3.addActionListener(this);
        del4.addActionListener(this);
        del5.addActionListener(this);
    }
	
	public void actionPerformed(ActionEvent e) {
		if(e.getSource()==addNote) {
			if(dem>=0||dem<5) {
				dem++;
			}
			if(dem==1) {
				del1.setVisible(true);
				TF1.setVisible(true);
			}
			if(dem==2) {
				del2.setVisible(true);
				TF2.setVisible(true);
			}
			if(dem==3) {
				del3.setVisible(true);
				TF3.setVisible(true);
			}
			if(dem==4) {
				del4.setVisible(true);
				TF4.setVisible(true);
			}
			if(dem==5) {
				del5.setVisible(true);
				TF5.setVisible(true);
			}
		}
		
		//DEL
		if(e.getSource()==del1) {
			dem--;
			TF1.setVisible(false);
			del1.setVisible(false);
		}
		if(e.getSource()==del2) {
			dem--;
			TF2.setVisible(false);
			del2.setVisible(false);
		}
		if(e.getSource()==del3) {
			dem--;
			TF3.setVisible(false);
			del3.setVisible(false);
		}
		if(e.getSource()==del4) {
			dem--;
			TF4.setVisible(false);
			del4.setVisible(false);
		}
		if(e.getSource()==del5) {
			dem--;
			TF5.setVisible(false);
			del5.setVisible(false);
		}
			
		if(e.getSource()==visibleAddNote) {
			if(visibleAddNote.getText()=="Are you have work?") {
				visibleAddNote.setText("Hide your note work!");
				addNote.setVisible(true);
//				del1.setVisible(true);
//				del2.setVisible(true);
//				del3.setVisible(true);
//				del4.setVisible(true);
//				del5.setVisible(true);
//				TF1.setVisible(true);
//				TF2.setVisible(true);
//				TF3.setVisible(true);
//				TF4.setVisible(true);
//				TF5.setVisible(true);
			}
			else if(visibleAddNote.getText()=="Hide your note work!") {
				visibleAddNote.setText("Are you have work?");
				addNote.setVisible(false);
//				del1.setVisible(false);
//				del2.setVisible(false);
//				del3.setVisible(false);
//				del4.setVisible(false);
//				del5.setVisible(false);
//				TF1.setVisible(false);
//				TF2.setVisible(false);
//				TF3.setVisible(false);
//				TF4.setVisible(false);
//				TF5.setVisible(false);
			}
			
		}
	}
}


