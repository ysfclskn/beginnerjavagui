# beginnerjavagui
Java GUI Beginner
import javax.swing.ImageIcon;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JPanel;

public class BtAction {
public static void main(String args[]){
	JFrame.setDefaultLookAndFeelDecorated(true); // Daha Güzel Dekorasyon JFrame için
	JFrame frame = new JFrame("GUI BUTTON/ACTION");// JFrame oluşturuldu.

	
	JPanel GUI = new JPanel();/* JFrame içinde GUI adlı JPANEL oluşturuldu.*/
	GUI.setLayout(null);/*GUI adlı JPanel'in düzeni belirsiz yapıldı.*/
	
	JPanel dugmeler = new JPanel(); /* Dugmeler adında 200x200 bir panel oluşturuldu*/
	dugmeler.setLayout(null);/* Düzen: Belirsiz */
	dugmeler.setLocation(5,5);/* Mevkisi 5 ,5 */
	dugmeler.setSize(200,200);/* Genişlik : 200 , Boy : 200 */
	GUI.add(dugmeler);/* GUI adlı panele dugmeler adlı panel eklendi */
	
	JButton jb1 = new JButton(); /* Buton oluşturuldu */
	jb1.setSize(150,20); 
	jb1.setText("Buna Bas!"); /* Butonun yazısı ayarlandı */
	jb1.setLocation(50,5);
	jb1.setHorizontalAlignment(2); /* Yatay Hizalama ( 0:ORTA , 2:SOL , 4:SAĞ)*/
	dugmeler.add(jb1);/* jb1 adlı buton dugmeler adlı panele eklendi */
	
	JButton jb2 = new JButton();/* Buton oluşturuldu */
	jb2.setSize(150,20);
	jb2.setText("Buna Basma!");
	jb2.setLocation(50,30);
	jb2.setHorizontalAlignment(4);/* Yatay Hizalama ( 0:ORTA , 2:SOL , 4:SAĞ)*/
	dugmeler.add(jb2);/* jb2 adlı buton dugmeler adlı panele eklendi */
	
	ImageIcon img1 = new ImageIcon ("C:/Users/YsF/workspace/ButtonAction/src/images/accept.png");
	/* ImageIcon komutuyla dışarda bir image dosyası alındı */
	JButton jb3 = new JButton("Onaylandı!" , img1); /*Doğru: JButton(String, image)   || Yanlış : JButton(image , String)*/
	jb3.setSize(150, 50);
	jb3.setHorizontalTextPosition(2);/* Hem text hem image bulunduğu için textin image e göre mevkisi ayarlandı */
	jb3.setLocation(50, 60);
	dugmeler.add(jb3);
	
	
	
	frame.setSize(300, 300);/*JFrame boyutu ayarlandı*/
	frame.setLocation(500,200);/*JFrame açılma mevkisi belirlendi*/
	frame.setResizable(false);/*JFrame'in boyutlandırılabilirliği kapatıldı*/
	frame.add(GUI);/*GUI adlı panel JFrame'e eklendi */
	frame.setVisible(true);/* JFrame görünür yapıldı */
	
	
}
}
