
platform :ios, '12.0'

source 'https://github.com/CocoaPods/Specs.git'

inhibit_all_warnings!

post_install do |installer|
    installer.pods_project.targets.each do |target|
      if target.respond_to?(:product_type) and target.product_type == "com.apple.product-type.bundle"
        target.build_configurations.each do |config|
            config.build_settings['CODE_SIGNING_ALLOWED'] = 'NO'
        end
      end
    end
end

target 'AppConfig' do
    # Networking
    pod 'Alamofire'
end