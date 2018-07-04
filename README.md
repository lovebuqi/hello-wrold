# hello-wrold
beginner

作为一个初学者 ，英文蹩脚很痛苦啊。

import java.io.File;

public class day20_DiGuiTest2 {

	public static void main(String[] args) {
	
		//add file
		File file = new File("D:\\FileDB1");//Don't use a C disk
		
		DiGuiDel(file);
	}
	//delete Method
	public static void DiGuiDel(File file) {
		File[] filearray = file.listFiles();
		if (filearray != null) {
			for (File file1 : filearray) {
				if (file1.isFile()) {
					System.out.println(file1 + "---" + file1.delete());
				} else  {
					DiGuiDel(file1);
				}
			}
		}
		System.out.println(file + "---" + file.delete());
	}
}
