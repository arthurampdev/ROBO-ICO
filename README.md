# ROBO-ICO

package Leclerc;
import robocode.*;
//import java.awt.Color;

// API help : https://robocode.sourceforge.io/docs/robocode/robocode/Robot.html

/**
 * Driving_like_Leclerc - a robot by (your name here)
 */
public class Driving_like_Leclerc extends AdvancedRobot
{   
	/**
	 * run: Driving_like_Leclerc's default behavior
	 */
	public void run() {
		// Initialization of the robot should be put here

		// After trying out your robot, try uncommenting the import at the top,
		// and the next line:

		// setColors(Color.red,Color.blue,Color.green); // body,gun,radar

		// Robot main loop
		while(true) {
			// Replace the next 4 lines with any behavior you would like
			for (int combmov=0;combmov<8;combmov++)
			{
			  setAhead(100);
			  setTurnLeft(150);
			  execute();
			  turnGunLeft(90);
			}
			for (int combesq=15;combesq>0;combesq--)
			{
			  setAhead(100);
			  setTurnRight(120);
			  execute();
			  turnGunRight(90);
			}
		}
	}

	/**
	 * onScannedRobot: What to do when you see another robot
	 */
	public void onScannedRobot(ScannedRobotEvent e) {
		// Replace the next line with any behavior you would like
        fire(1);
	}

	/**
	 * onHitByBullet: What to do when you're hit by a bullet
	 */
	public void onHitByBullet(HitByBulletEvent e) {
		// Replace the next line with any behavior you would like
		setBack(20);
		setAhead(100);
		execute();
	}
	
	/**
	 * onHitWall: What to do when you hit a wall
	 */
	public void onHitWall(HitWallEvent e) {
		// Replace the next line with any behavior you would like
		back(40);
		turnRight(10);
		ahead(30);
	}	
	public void onHitRobot(HitRobotEvent e) {
		back(150);
	}

}
