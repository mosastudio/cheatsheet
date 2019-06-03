## UIKit

```Swift
open class UIViewController : UIResponder, NSCoding, UIAppearanceContainer, UITraitEnvironment, UIContentContainer, UIFocusEnvironment {
    open func viewDidLoad()
    open func viewWillAppear(_ animated: Bool)
    open func viewDidAppear(_ animated: Bool)
    open func viewWillDisappear(_ animated: Bool)
    open func viewDidDisappear(_ animated: Bool)
    open func viewWillLayoutSubviews()
    open func viewDidLayoutSubviews()    
}

open class UIControl : UIView {
    open func beginTracking(_ touch: UITouch, with event: UIEvent?) -> Bool
    open func continueTracking(_ touch: UITouch, with event: UIEvent?) -> Bool
    open func endTracking(_ touch: UITouch?, with event: UIEvent?)
    open func cancelTracking(with event: UIEvent?)

    open func addTarget(_ target: Any?, action: Selector, for controlEvents: UIControl.Event)
}

open class UIView : UIResponder, NSCoding, UIAppearance, UIAppearanceContainer, UIDynamicItem, UITraitEnvironment, UICoordinateSpace, UIFocusItem, UIFocusItemContainer, CALayerDelegate {
    open var isExclusiveTouch: Bool
}

open class UIResponder : NSObject, UIResponderStandardEditActions {
    open func touchesBegan(_ touches: Set<UITouch>, with event: UIEvent?)
    open func touchesMoved(_ touches: Set<UITouch>, with event: UIEvent?)
    open func touchesEnded(_ touches: Set<UITouch>, with event: UIEvent?)
    open func touchesCancelled(_ touches: Set<UITouch>, with event: UIEvent?)
}

// UIControl.Event
public struct Event : OptionSet {
    public static var touchDown: UIControl.Event { get }
    public static var touchUpInside: UIControl.Event { get }
    public static var touchUpOutside: UIControl.Event { get }
    public static var valueChanged: UIControl.Event { get }    // slider, etc.
}

open class UILabel : UIView, NSCoding, UIContentSizeCategoryAdjusting {
}
open class UITextField : UIControl, UITextInput, NSCoding, UIContentSizeCategoryAdjusting {
}
open class UITextView : UIScrollView, UITextInput, UIContentSizeCategoryAdjusting {
}
open class UITableView : UIScrollView, NSCoding, UIDataSourceTranslating {
}
open class UICollectionView : UIScrollView, UIDataSourceTranslating {
}
```

* Push

```
    navigationController.pushViewController(vc, animated: true)
```

* present

```
    self.present(vc, animated: true, completion: nil)
```

* addSubView

```
    self.view.addSubview(customView)
```

```
    if let window = UIApplication.shared.keyWindow {
        window.addSubview(customView);
    }
```

* Dialog, similar as UIAlertController
  * [UIAlertController class ref.](https://developer.apple.com/documentation/uikit/uialertcontroller#//apple_ref/doc/uid/TP40014538-CH1-SW2), The UIAlertController class is intended to be used as-is and does not support subclassing. The view hierarchy for this class is private and must not be modified.
  * Progress HUD
    * [MBProgressHUD](https://github.com/jdg/MBProgressHUD)
      * [MBProgressHUD-WJExtension](https://github.com/WJCha/MBProgressHUD-WJExtension), using UIBezierPath, CAShapeLayer, CABasicAnimation
    * [SVProgressHUD](https://github.com/SVProgressHUD/SVProgressHUD)
  * Alert View / Alert Controller
    * [SCLAlertView, Swift](https://github.com/vikmeup/SCLAlertView-Swift)
    * [SCLAlertView, ObjC](https://github.com/dogo/SCLAlertView)
    * [SDCAlertView](https://github.com/sberrevoets/SDCAlertView)
    * [PopupDialog](https://github.com/orderella/PopupDialog)  
    * [PMAlertController](https://github.com/pmusolino/PMAlertController)
    * [SwiftMessages](https://github.com/SwiftKickMobile/SwiftMessages)
