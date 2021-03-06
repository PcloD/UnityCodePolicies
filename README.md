# UnityCodePolicies
## Intro
The guide is based on my experiences , recommendations from developers and colleges. When doing code reviews always check for these things and if there is an issue then let them know and reference this guide. If you have suggestions or questions then feel free to leave messages.


## Members
Use upper camel case for public members, and lower camel case for others.
Named protected, internal, and private members with prefix "m_".

#### Examples
```
public int PublicInt;
public float PublicFloat;
public bool PublicBool;

internal int m_internalInt;
internal float m_internalFloat;
internal bool m_internalBool;

protected int m_protectedInt;
protected float m_protectedFloat;
protected bool m_protectedBool;

private int m_privateInt;
private float m_privateFloat;
private bool m_privateBool;
```


## const and readonly
Named const and readonly members in CAPITAL letter and split the letter with "_";

#### Examples
```
private const int CONST_INT = 1;
public const string DOCUMENT_NAME = "UnityScriptPolicies";
```


## Methods
Named methods with the upper camel case.

#### Examples
```
public void FirstMethod()  
{  
    
}  
```


## Braces
Always seperated the open brace or close brace in a new line.
If you are using if/for or other things where braces are optional for the body always add the braces for it.

#### Examples
```
using UnityEngine;  
    
public class BraceExample : MonoBehaviour    
{    
    private void Start ()    
    {    
        for(int i = 0; i < 10; i++)    
        {    
            Debug.Log(i);    
        }    
    }    
    
    private void Update ()    
    {    
        if(!CanUpdate())    
        {    
            return;    
        }    
    
        //TODO: Update    
    }    
    
    private bool CanUpdate()    
    {    
        return true;    
    }    
}    
```


## interface
Named the interface class with prefix "I".

#### Examples
```
public interface IUpdate  
{  
  
}  
  
public interface IFixedUpdate  
{  
  
}
```


## Action, Delegate, Event, and Func
Named Action, delegate, event, and Func with prefix "On" in methods and "on" in members.

#### Examples
```
public delegate void OnPlayerHealthPointUpdate(float hp);
public Action onAction;
```


## Null Check
Always do the null check.

#### Examples
```
private GameObject m_target;  
  
private void Update()  
{  
    if(m_target == null)  
    {  
        return;  
    }  
  
    //TODO: Update the target  
}  
```


## UI (UGUI)
Use the component's name as the suffix.

#### Examples
| Component  | Policy              | Hierarchy Example  | Public Member Example | Private Member Example |
|------------|---------------------|--------------------|-----------------------|------------------------|
| Text       | [Feature]Text       | TitleText          | TitleText             | m_titleText            |
| Image      | [Feature]Image      | CloseImage         | CloseImage            | m_closeImage           |
| RawImage   | [Feature]RawImage   | BackgroundRawImage | BackgroundRawImage    | m_backgroundRawImage   |
| Button     | [Feature]Button     | PlayButton         | PlayButton            | m_playButton           |
| Toggle     | [Feature]Toggle     | BGMToggle          | BGMToggle             | m_bgmToggle            |
| Slider     | [Feature]Slider     | HPSlider           | HPSlider              | m_hpSlider             |
| Scrollbar  | [Feature]Scrollbar  | ItemScrollbar      | ItemScrollbar         | m_itemScrollbar        |
| Dropdown   | [Feature]Dropdown   | WeaponDropdown     | WeaponDropdown        | m_weaponDropdown       |
| InputField | [Feature]InputField | PasswordInputField | PasswordInputField    | m_passwordInputField   |
| Canvas     | [Feature]Canvas     | MainCanvas         | MainCanvas            | m_mainCanvas           |
