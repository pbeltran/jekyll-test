--- layout: post title: Instalar Smart Board 480 en Ubuntu date:
'2015-02-27T20:04:00.000+01:00' author: Pablo Beltrán-Pellicer tags:
modified\_time: '2015-02-27T20:04:23.632+01:00' --- Aquí los pasos:  
http://www.javiercarrasco.es/2013/02/27/instalar-pizarra-digital-smart-board-en-ubuntu-12-04/  
  
  
Installing SMART Software  
  
1.             Download SMART Software Debian Plain Files from
http://downloads.smarttech.com/software/nb/11linux/11sp1/smartnotebook11sp1\_deb\_filesv3.tar.gz
 to ~/Downloads  
  
2.             Untar the smartnotebook11sp1\_deb\_filesv3.tar.gz file by
using the command  
  
                                                                    tar
xvfz ~/Downloads/smartnotebook11sp1\_deb\_filesv3.tar.gz  
  
                                                                       
            and press the Enter key  
  
3.             Enter the command  
  
                                                                    sudo
dpkg –i ~/Downloads/ smartnotebook11sp1\_deb\_filesv3/smart-\*.deb  
  
                                                                       
             and press the Enter key  
  
Installing Packages for the SB480 Whiteboard  
  
1.                                     Install
xf86-input-nextwindow-wheezy by entering the command  
  
                                                                  sudo
dpkg –i xf86-input-nextwindow-wheezy\_0.3.4~wheezy1\_i386.deb  
  
                                                                       
         and press Enter  
  
2.                                     Now install nwfermi by entering
the command  
  
                                                                sudo
dpkg –i nwfermi-0.6.5.1\_i386.deb  
  
                                                                       
          and press Enter  
  
  
xorg??  
  
Para el <span
style="color: #333333; font-family: HelveticaNeue-Light, 'Helvetica Neue Light', 'Helvetica Neue', Roboto, Helvetica, Arial, sans-serif;">sudo
./customize.sh files es necesario el dpkg-sig</span>  
<span
style="color: #333333; font-family: HelveticaNeue-Light, 'Helvetica Neue Light', 'Helvetica Neue', Roboto, Helvetica, Arial, sans-serif;">  
</span><span
style="color: #333333; font-family: HelveticaNeue-Light, Helvetica Neue Light, Helvetica Neue, Roboto, Helvetica, Arial, sans-serif;">In
order to get the SMART Board™ SB480 Interactive Whiteboard to work
properly with Ubuntu Linux version 12.04.4 you need to use the
xf86-nextwindow-input-wheezy package instead of the
xf86-nextwindow-input-precise package.</span>
