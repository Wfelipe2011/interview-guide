# Swift

- O que é Swift?
  - [R]: Swift é uma linguagem de programação criada pela Apple para desenvolvimento de aplicativos para iOS, macOS, watchOS, tvOS e Linux.

- Auto Layout
  - [R]: É um sistema de layout que permite que os elementos de uma interface sejam posicionados de forma dinâmica, de acordo com o tamanho da tela do dispositivo.
  - EX: Um botão que está no canto inferior direito da tela, deve ficar no canto inferior direito da tela, mesmo que o usuário mude o tamanho da tela.

- Quais os principais tipos de dados em Swift?
  - [R]: Int, Double, Float, Bool, String, Character, Array, Dictionary, Set, Tuple, Optionals

- O que é Tagueamento?
  - [R]: É uma forma de identificar um elemento de uma interface, para que ele possa ser manipulado pelo código.
  - EX: Um botão pode ser identificado pelo seu título, por um ícone ou por um identificador único.

[Artigo sobre Storyboard - Xib - ViewCode](https://www.alura.com.br/artigos/ios-swift-diferencas-construcao-layouts-storyboard-xib-view-code#:~:text=xib%20representa%20uma%20%C3%BAnica%20view,uma%20view%2C%20assim%20por%20diante.)

- O que é Storyboard?
  - [R]: É um arquivo que contém a interface de um aplicativo, que pode ser criado pelo Interface Builder.
  - EX: Um arquivo .storyboard contém todas as telas de um aplicativo, e cada tela contém todos os elementos da interface.

- O que é Interface Builder?
  - [R]: É uma ferramenta que permite a criação de interfaces gráficas para aplicativos.
  - EX: O Interface Builder é usado para criar telas de aplicativos, e cada tela é um arquivo .storyboard.

- O que é Xib?
  - [R]: É um arquivo que contém a interface de um elemento de interface, que pode ser criado pelo Interface Builder.
  - EX: Um arquivo .xib contém a interface de um botão, de um label, de um text field, etc.

- O que é View Code?
  - [R]: É uma forma de desenvolver interfaces sem utilizar Storyboards ou XIBs.  
  - EX:

    ```swift
    class ViewController: UIViewController {
        let label = UILabel()
        let button = UIButton()
        
        override func viewDidLoad() {
            super.viewDidLoad()
            view.backgroundColor = .white
            setupLabel()
            setupButton()
        }
        
        func setupLabel() {
            label.text = "Hello World"
            label.textColor = .black
            label.font = UIFont.systemFont(ofSize: 24)
            label.textAlignment = .center
            label.translatesAutoresizingMaskIntoConstraints = false
            view.addSubview(label)
            
            NSLayoutConstraint.activate([
                label.topAnchor.constraint(equalTo: view.topAnchor, constant: 100),
                label.leadingAnchor.constraint(equalTo: view.leadingAnchor, constant: 16),
                label.trailingAnchor.constraint(equalTo: view.trailingAnchor, constant: -16)
            ])
        }
        
        func setupButton() {
            button.setTitle("Click me", for: .normal)
            button.setTitleColor(.black, for: .normal)
            button.backgroundColor = .white
            button.layer.cornerRadius = 8
            button.layer.borderWidth = 1
            button.layer.borderColor = UIColor.black.cgColor
            button.translatesAutoresizingMaskIntoConstraints = false
            view.addSubview(button)
            
            NSLayoutConstraint.activate([
                button.topAnchor.constraint(equalTo: label.bottomAnchor, constant: 16),
                button.leadingAnchor.constraint(equalTo: view.leadingAnchor, constant: 16),
                button.trailingAnchor.constraint(equalTo: view.trailingAnchor, constant: -16),
                button.heightAnchor.constraint(equalToConstant: 50)
            ])
        }
    }
    ```

- O que é Camada Nativa de Network?
  - [R]: É uma camada nativa de network que permite fazer requisições HTTP e HTTPS.
  - EX:

    ```swift
    let url = URL(string: "https://jsonplaceholder.typicode.com/posts")!
    let task = URLSession.shared.dataTask(with: url) { data, response, error in
        guard let data = data, error == nil else {
            print(error?.localizedDescription ?? "No data")
            return
        }
        let responseJSON = try? JSONSerialization.jsonObject(with: data, options: [])
        if let responseJSON = responseJSON as? [String: Any] {
            print(responseJSON)
        }
    }
    task.resume()
    ```

- O que é Cocoa Pods?
  - [R]: É um gerenciador de dependências para projetos Swift e Objective-C.
  - EX: `pod 'Alamofire'`

- O que é Alamofire?
  - [R]: É uma biblioteca para requisições HTTP e HTTPS.
  - EX:

    ```swift
    AF.request("https://jsonplaceholder.typicode.com/posts").responseJSON { response in
        debugPrint(response)
    }
    ```

- O que é Promisekit?
  - [R]: É uma biblioteca para trabalhar com promises.
  - EX:

    ```swift
    firstly {
        AF.request("https://jsonplaceholder.typicode.com/posts")
    }.done { response in
        debugPrint(response)
    }.catch { error in
        debugPrint(error)
    }
    ```

- Como fazer uma view ocupar toda a tela?
  - [R]: Usando o `fillSuperview()`
  - EX: `view.fillSuperview()`
  - [R]: Usando o `fillSuperviewSafeArea()`
  - EX: `view.fillSuperviewSafeArea()`
  - [R]: Usando o `fillSuperviewSafeAreaLayoutGuide()`
  - EX: `view.fillSuperviewSafeAreaLayoutGuide()`

- Como consumir uma API?
  - [R]: Usando o `URLSession`
  - EX: `URLSession.shared.dataTask(with: url) { (data, response, error) in }`
  - [R]: Usando o `Alamofire`
  - EX: `Alamofire.request(url).responseJSON { (response) in }`

- Como exibir uma imagem na tela?
  - [R]: Usando o `UIImageView`
  - EX: `let imageView = UIImageView(image: image)`
  - [R]: Usando o `Kingfisher`
  - EX: `imageView.kf.setImage(with: url)`
  - [R]: Usando o `SDWebImage`
  - EX: `imageView.sd_setImage(with: url)`
  - [R]: Usando o `Nuke`
  - EX: `imageView.loadImage(with: url)`
  - [R]: Usando o `AlamofireImage`
  - EX: `imageView.af_setImage(withURL: url)`
  - [R]: Usando o `SwiftUI`
  - EX: `Image(uiImage: image)`

- Como fazer uma animação?
  - [R]: Usando o `UIView.animate(withDuration:animations:)`
  - EX: `UIView.animate(withDuration: 0.5) { view.alpha = 0 }`
  - [R]: Usando o `UIViewPropertyAnimator`
  - EX: `let animator = UIViewPropertyAnimator(duration: 0.5, curve: .easeInOut) { view.alpha = 0 }`
  - [R]: Usando o `UIViewPropertyAnimator`
  - EX: `let animator = UIViewPropertyAnimator(duration: 0.5, curve: .easeInOut) { view.alpha = 0 }`
  - [R]: Usando o `UIViewPropertyAnimator`
  - EX: `let animator = UIViewPropertyAnimator(duration: 0.5, curve: .easeInOut) { view.alpha = 0 }`
  - [R]: Usando o `UIViewPropertyAnimator`
  - EX: `let animator = UIViewPropertyAnimator(duration: 0.5, curve: .easeInOut) { view.alpha = 0 }`
  - [R]: Usando o `UIViewPropertyAnimator`
  - EX: `let animator = UIViewPropertyAnimator(duration: 0.5, curve: .easeInOut) { view.alpha = 0 }`
  - [R]: Usando o `UIViewPropertyAnimator`
  - EX: `let animator = UIViewPropertyAnimator(duration: 0.5, curve: .easeInOut) { view.alpha = 0 }`
  - [R]: Usando o `UIViewPropertyAnimator`
  - EX: `let animator = UIViewPropertyAnimator(duration: 0.5, curve: .easeInOut) { view.alpha = 0 }`
  - [R]: Usando o `UIViewPropertyAnimator`
  - EX: `let animator = UIViewPropertyAnimator(duration: 0.5, curve: .easeInOut) { view.alpha = 0 }`
  - [R]: Usando o `UIViewPropertyAnimator`
  - EX: `let animator = UIViewPropertyAnimator(duration: 0.5, curve: .easeInOut) { view.alpha = 0 }`
  - [R]: Usando o `UIViewPropertyAnimator`
  - EX: `let animator = UIViewPropertyAnimator(duration: 0.5, curve: .easeInOut) { view.alpha = 0 }`

- Como é build do app?
  - [R]: O Xcode compila o código Swift para código nativo, que é executado pelo sistema operacional.

- Como é o processo de deploy do app?
  - [R]: O Xcode gera um arquivo .ipa, que é enviado para a App Store.
