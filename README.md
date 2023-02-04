# CustomTabBarController
I build my reusable custom Tab Bar Controller\
<img src="https://github.com/ahmed-yamany/CustomTabBarController/blob/main/images/Screenshot%202023-02-04%20at%205.14.56%20AM.png" width="300" height="400">
<img src="https://github.com/ahmed-yamany/CustomTabBarController/blob/main/images/Screenshot%202023-02-04%20at%205.15.19%20AM.png" width="300" height="400">

The usage is like the default UITabBarController in UIKit

'''swift

      class AppTabBarController: CustomTabBarController {

          override func viewDidLoad() {
              super.viewDidLoad()
              let vc1 = ViewController()
              vc1.tabBarItem = UITabBarItem(title: nil, image: UIImage(systemName: "house"), selectedImage: UIImage(systemName: "house.fill"))

              let vc2 = ViewController()
              vc2.tabBarItem = UITabBarItem(title: nil, image: UIImage(systemName: "trash"), selectedImage: UIImage(systemName: "trash.fill"))

              let vc3 = ViewController()
              vc3.tabBarItem = UITabBarItem(title: nil, image: UIImage(systemName: "folder.badge.plus"), selectedImage: UIImage(systemName: "folder.badge.plus.fill"))
              let vc4 = ViewController()
              vc4.tabBarItem = UITabBarItem(title: nil, image: UIImage(systemName: "trash"), selectedImage: UIImage(systemName: "trash.fill"))

              let vc5 = ViewController()
              vc5.tabBarItem = UITabBarItem(title: nil, image: UIImage(systemName: "trash"), selectedImage: UIImage(systemName: "trash.fill"))

              viewControllers = [vc1, vc2, vc3, vc4, vc5]

          }
      }
  

'''

<img src="https://github.com/ahmed-yamany/CustomTabBarController/blob/main/images/Screenshot%202023-02-04%20at%205.30.21%20AM.png" width="300" height="400">


you can change the size "width and height" of the tab bar, cornerRadius, background, or tintColor

'''swift

      tabBar.size = CGSize(width: 300, height: 60)
      tabBar.layer.cornerRadius = 30
      tabBar.backgroundColor = .systemCyan
      tintColor = .black
      
'''

<img src="https://github.com/ahmed-yamany/CustomTabBarController/blob/main/images/Screenshot%202023-02-04%20at%205.37.00%20AM.png" width="300" height="400">


you can change the layout of the tabBar by override layoutTabBar method
and add padding from the bottom

'''swift

        override func layoutTabBar(_ tabBar: TabBar) {
            tabBar.centerXAnchor.constraint(equalTo: view.centerXAnchor).isActive = true
            tabBar.bottomAnchor.constraint(equalTo: view.bottomAnchor, constant: -40).isActive = true
        }

'''
<img src="https://github.com/ahmed-yamany/CustomTabBarController/blob/main/images/Screenshot%202023-02-04%20at%205.46.24%20AM.png" width="300" height="400">

or center it to the screen 😅 😂

'''swift
          
          override func layoutTabBar(_ tabBar: TabBar) {
              tabBar.centerXAnchor.constraint(equalTo: view.centerXAnchor).isActive = true
              tabBar.centerYAnchor.constraint(equalTo: view.centerYAnchor).isActive = true
          }

'''

<img src="https://github.com/ahmed-yamany/CustomTabBarController/blob/main/images/Screenshot%202023-02-04%20at%205.50.06%20AM.png" width="300" height="400">

you can add a custom background view to the tabBar

'''swift

        let bview = BackgroundView()
        tabBar.addSubview(bview)
        bview.translatesAutoresizingMaskIntoConstraints = false
        bview.topAnchor.constraint(equalTo: tabBar.topAnchor).isActive = true
        bview.bottomAnchor.constraint(equalTo: tabBar.bottomAnchor).isActive = true
        bview.leadingAnchor.constraint(equalTo: tabBar.leadingAnchor).isActive = true
        bview.trailingAnchor.constraint(equalTo: tabBar.trailingAnchor).isActive = true


'''
<img src="https://github.com/ahmed-yamany/CustomTabBarController/blob/main/images/Screenshot%202023-02-04%20at%205.56.15%20AM.png" width="300" height="400">


I wish this helps some one 
I wish you give me feedback
Thanks
