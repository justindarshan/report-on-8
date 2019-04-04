# report-on-8
project




as per the design of our project we written code for the flash screen of the project
in the sense the screen which appears first while opening our app
and the logo of the app for the voice assistant for visually impaired people
package eighteen.cmp.mani.friendlyvission;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;

import java.util.Timer;
import java.util.TimerTask;

public class Splash extends AppCompatActivity {
Timer t;
    TimerTask tt;
    long delay=3000;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.splash);
        Timer t=new Timer();
        TimerTask tt =new TimerTask() {
            @Override
            public void run() {

                Intent i=new Intent(Splash.this,HomePage.class);
                startActivity(i);
                finish();
            }
        };
        t.schedule(tt,delay);
    }
}
