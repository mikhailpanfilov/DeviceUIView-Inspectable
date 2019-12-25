## [#`UILabel`]()

```swift
@IBDesignable class <#IPad#>Label: UILabel {
    
    @IBInspectable var <#iPad#>FontSize: CGFloat = 0.0 {
        didSet { deviceConstant(DeviceType.iPad, value: iPadFontSize) }
    }
    
    // Helpers
    
    open func deviceConstant(_ currentDevice: Bool, value: CGFloat) {
        if currentDevice, let currentFont = font {
            font = UIFont(name: currentFont.fontName, size: value)
        }
    }
}
```

## [#`UIView`]()

```swift
@IBDesignable class <#IPad#>View: UIView {
    
    @IBInspectable var <#iPad#>CornerRadius: CGFloat = 0.0 {
        didSet { deviceConstant(DeviceType.iPad, value: iPadCornerRadius) }
    }
    
    @IBInspectable var <#iPhone#>CornerRadius: CGFloat = 0.0 {
        didSet { deviceConstant(DeviceType.iPhone, value: iPhoneCornerRadius) }
    }
    
    // Helpers
    
    open func deviceConstant(_ currentDevice: Bool, value: CGFloat) {
        if currentDevice {
            layer.cornerRadius = value
        }
    }
}
```

## [#`UIButton`]()

```swift
@IBDesignable class <#IPad#>Button: UIButton {
    
    @IBInspectable var <#iPad#>FontSize: CGFloat = 0.0 {
        didSet { deviceConstant(DeviceType.iPad, value: iPadFontSize) }
    }
    
    // Helpers
    
    open func deviceConstant(_ currentDevice: Bool, value: CGFloat) {
        if currentDevice, let currentButtonFont = titleLabel?.font {
            titleLabel?.font = UIFont(name: currentButtonFont.fontName, size: value )
        }
    }
}
```

## [#`UIStackView`]()

```swift
@IBDesignable class <#IPad#>StackView: UIStackView {
    
    @IBInspectable var <#iPad#>Spacing: CGFloat = 0.0 {
        didSet { deviceConstant(DeviceType.iPad, value: iPadSpacing) }
    }
    
    // Helpers
    
    open func deviceConstant(_ currentDevice: Bool, value: CGFloat) {
        if currentDevice {
            spacing = value
        }
    }
}
```


