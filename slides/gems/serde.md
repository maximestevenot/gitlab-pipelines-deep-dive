## Serde
<img src="lib/images/serde.svg" style="height:40vh"/>  
[📒](https://serde.rs/) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=4aaae8de88ab6c997530802807b5fab3)

<!--
use serde::*;
#[derive(new, Clone, Debug, Serialize, Deserialize)]
#[serde(default)]
struct Dog { name: String, color: String }
impl Default for Dog {
    fn default() -> Self { Dog { name: String::new(), color: String::new() } }
}
#[test]
fn test() {
    let dog = Dog::new("Rex".to_string(), "black".to_string());
    let yaml_dog = serde_yaml::to_string(&dog).unwrap();
    let json_dog = serde_json::to_string(&dog).unwrap();
    println!("Yaml dog {:#?}", yaml_dog);
    println!("Json dog {:#?}", json_dog);
    let real_yaml_dog: Dog = serde_yaml::from_str(&yaml_dog).unwrap();
    let real_json_dog: Dog = serde_json::from_str(&json_dog).unwrap();
    println!("Real Yaml dog {:#?}", real_yaml_dog);
    println!("Real Json dog {:#?}", real_json_dog);
}
-->