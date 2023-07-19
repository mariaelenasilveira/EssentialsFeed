# EssentialsFeed


```
class FirstViewController: UIViewController {
    
    var coordinator: MainCoordinator
    
    private var nextViewButtom: UIButton = {
        let buttom = UIButton()
        buttom.setTitle("Next View", for: .normal)
        buttom.addTarget(self, action: #selector(tapedNextView), for: .touchUpInside)
        buttom.translatesAutoresizingMaskIntoConstraints = false
        return buttom
    }()
    
    init(coordinator: MainCoordinator) {
        self.coordinator = coordinator
        super.init(nibName: nil, bundle: nil)
    }
    
    required init?(coder: NSCoder) {
        fatalError("init(coder:) has not been implemented")
    }
    
    override func viewDidLoad() {
        super.viewDidLoad()
        setupView()
    }
    
    @objc
    func tapedNextView(){
        self.coordinator.toSecondView()
    }
}
```
