# MP-TK-ODEV-4-
MP TK ODEV 4 
package com.example.myapplication;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
public class MainActivity extends AppCompatActivity{
private ActivityMainBinding;

ArrayList<Gorsel> GorselArrayList;

int SeciliSiraNo;

@Override

protected coid onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
binding = ActivityMainBinding.inflate(getLayoutInflater());
View view = biding.getrobot();
setContentWiew(View);

gorselArrayList = new ArrayList <>();

Gorsel Balon = new Gorsel( Bilgi: "Sarı Balon" , SiraNo 1,R.Drawble.Balon);
Gorsel Cicek = new Gorsel( Bilgi: "Mavi Cicek" , SiraNo 2,R.Drawble.Cicek);
Gorsel Kelebek = new Gorsel( Bilgi: "Mavi Kelebek" , SiraNo 3,R.Drawble.Kelebek);
Gorsel Kus = new Gorsel( Bilgi: "Yuvada Kuş" , SiraNo 4,R.Drawble.Kus);

GorselArrayList.add(Balon);
GorselArrayList.add(Cicek);
GorselArrayList.add(Kelebek);
GorselArrayList.add(Kus);

binding.imageViewGoesel.setInageResource(GorselArraylist.get(0).Foto);
binding.tectViewBilgi.setText("Bilgi ; " + GorselArrayList.get(0).Bilgi);
SeciliSiraNo=0;

public void geriGelme(View view){
 if(SeciliSiraNo>0){
 SeciliSiraNo--;
 binding.imageViewGorsel.setImageResource(GorselArrayList.get(SeciliSiraNo).Foto);
 binding.textViewBilgi.setText(“Bilgi : “ + GorselArrayList.get(SeciliSiraNo).Bilgi);
 }
}

public void ileriGitme(View view){
 if(seciliSiraNo<GorselArrayList.size()-1){
 SeciliSiraNo++;
 binding.imageViewGorsel.setImageResource(GorselArrayList.get(SeciliSiraNo).Foto);
 binding.textViewBilgi.setText(“Bilgi : “ + GorselArrayList.get(SeciliSiraNo).Bilgi);
 }
}
