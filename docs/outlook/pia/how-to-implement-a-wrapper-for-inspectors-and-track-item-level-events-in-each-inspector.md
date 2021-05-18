---
title: インスペクターのラッパーを実装し、インスペクターごとにアイテム レベルのイベントを追跡する
TOCTitle: Implement a wrapper for inspectors and track item-level events in each inspector
ms:assetid: 8021dd2b-c36c-492b-b281-783e85140ad8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184620(v=office.15)
ms:contentKeyID: 55119854
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a70aedf9a8803a2c990f07a77d4fc730f7263aae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320126"
---
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a><span data-ttu-id="3d0f4-102">インスペクターのラッパーを実装し、インスペクターごとにアイテム レベルのイベントを追跡する</span><span class="sxs-lookup"><span data-stu-id="3d0f4-102">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>

<span data-ttu-id="3d0f4-103">このトピックに含まれる 2 つのコード例では、[Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) コレクション用のラッパーを実装し、そのラッパーを使用してコレクション内の各 [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) オブジェクトでアイテムレベルのイベントを追跡する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-103">This topic contains two code examples that show how to implement a wrapper for an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) collection and to use that wrapper to track item-level events in each [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) object in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="3d0f4-104">例</span><span class="sxs-lookup"><span data-stu-id="3d0f4-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3d0f4-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="3d0f4-106">次の 2 つのコード例では、Connect クラスと OutlookInspector クラスの実装を行います。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-106">The following two code examples implement the Connect and OutlookInspector classes.</span></span> <span data-ttu-id="3d0f4-107">1 番目のコード例では **インスペクター** コレクションにラッパーを実装するために、ユーザーが Connect クラスに格納したメソッドとイベント ハンドラーを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-107">The first code example involves methods and event handlers you include in the Connect class to implement a wrapper for an **Inspectors** collection.</span></span> <span data-ttu-id="3d0f4-108">2 番目のコード例では、単純に **OutlookInspector** クラスを実装します。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-108">The second code example involves a simple implementation of the **OutlookInspector** class.</span></span>

<span data-ttu-id="3d0f4-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3d0f4-110">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3d0f4-111">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="3d0f4-112">次のコード例では、 [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) イベントは、新しいインスペクター ウィンドウの作成後、それが表示される前に発生しています。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-112">In the following code example, a [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) event occurs after a new inspector window has been created and before it is displayed.</span></span> <span data-ttu-id="3d0f4-113">新しいインスペクター ウィンドウは、ユーザーの操作でも作成できます。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-113">A user action may also create a new inspector window.</span></span> <span data-ttu-id="3d0f4-114">**Connect** クラスで insepctors という名前のクラス レベルのインスタンス変数が宣言され、**NewInspector** イベントが接続されます。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-114">A class-level instance variable named inspectors in the **Connect** class is declared, and a **NewInspector** event is hooked up.</span></span> 

<span data-ttu-id="3d0f4-115">inspectors\_NewInspector メソッドでは、新しいインスペクター ウィンドウが inspectorWindows リストが既にあるかどうかを **FindOutlookInspector** メソッドがチェックします。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-115">In the inspectors\_NewInspector method, the **FindOutlookInspector** method checks whether the new inspector window is already in the inspectorWindows list.</span></span> <span data-ttu-id="3d0f4-116">FindOutlookInspector により inspectorWindows 内で **Inspector** オブジェクトが検出されない場合、**AddInspector** メソッドは **OutlookInspector** クラスのインスタンスを inspectorWindows に追加します。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-116">If FindOutlookInspector does not find the **Inspector** object in inspectorWindows, the **AddInspector** method adds an instance of the **OutlookInspector** class to inspectorWindows.</span></span> <span data-ttu-id="3d0f4-117">**OutlookInspector** クラスを使用して、このインスペクター ウィンドウでイベントを発生させることができます。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-117">You can use the **OutlookInspector** class to raise events for this particular inspector window.</span></span> <span data-ttu-id="3d0f4-118">2 番目のコード例に **OutlookInspector** クラスの実装を示します。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-118">The implementation of the **OutlookInspector** class is shown in the second code example.</span></span>

```csharp
class Connect
{
    // Connect class-level Instance Variables
    // Outlook inspectors collection
    private Outlook.Inspectors inspectors;

    // Collection of tracked inspector windows              
    private List<OutlookInspector> inspectorWindows;    

    // Hook up NewInspector event
    inspectors.NewInspector += new 
        Outlook.InspectorsEvents_NewInspectorEventHandler(
        inspectors_NewInspector);

    // NewInspector event creates new instance of OutlookInspector
    void inspectors_NewInspector(Outlook.Inspector Inspector)
    {
        // Check to see if this is a new window you don't
        // already track
        OutlookInspector existingWindow = 
            FindOutlookInspector(Inspector);
        if (existingWindow == null)
        {
            AddInspector(Inspector);
        }
    }

    // Adds an instance of **OutlookInspector** class
    private void AddInspector(Outlook.Inspector inspector)
    {
        OutlookInspector window = new OutlookInspector(inspector);
        window.Close +=
            new EventHandler(WrappedInspectorWindow_Close);
    }

    // Looks up the window wrapper for a given Inspector 
    // window object
    private OutlookInspector FindOutlookInspector(object window)
    {
        foreach (OutlookInspector inspector in inspectorWindows)
        {
            if (inspector.Window == window)
            {
                return inspector;
            }
        }
        return null;
    }
}
```

<span data-ttu-id="3d0f4-119">次のコード例では、**OutlookInspector** クラスの実装が行われます。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-119">The following code example is an implementation of the **OutlookInspector** class.</span></span> <span data-ttu-id="3d0f4-120">このクラスを使用して、上記のコード例で示したインスペクター ウィンドウでイベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-120">This class is used to raise events for the inspector window from the preceding code example.</span></span> <span data-ttu-id="3d0f4-121">複数のインスペクター ウィンドウを同時に開いておくことができます。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-121">Multiple inspector windows can be open simultaneously.</span></span> <span data-ttu-id="3d0f4-122">[Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\))、[PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\))、[CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) などのアイテム レベルのイベントは、このクラス コンストラクターで接続すると追跡されます。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-122">Item-level events such as [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)), and [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) are tracked by hooking them up in this class constructor.</span></span> <span data-ttu-id="3d0f4-123">[ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) オブジェクト用の [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) イベントもこのクラス コンストラクターで接続されます。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-123">A [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) event for a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object is also hooked up in this class constructor.</span></span> <span data-ttu-id="3d0f4-124">必要に応じて、他のクラス レベル アイテムのインスタンス変数を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-124">You can define other class-level item instance variables as needed.</span></span> <span data-ttu-id="3d0f4-125">OutlookInspector コンストラクターで接続されたすべてのイベントは、OutlookInspectorWindow\_Close event ハンドラーで接続解除されます。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-125">All the events that were hooked up in the OutlookInspector constructor are unhooked in the OutlookInspectorWindow\_Close event handler.</span></span>

<span data-ttu-id="3d0f4-126">なお、オブジェクト モデルのレベルでは、**Outlook のインスペクター** オブジェクトはどの Outlook アイテムの種類にも固有ではありません。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-126">Note that at the object model level, an **Outlook inspector** object is not specific to any Outlook item type.</span></span> <span data-ttu-id="3d0f4-127">このコード サンプルでは、アイテムを連絡先アイテムとみなす前に、OutlookItem.Class プロパティを素早く呼び出してインスペクターの現在のアイテムのメッセージ クラスを確認するために、「[ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)」で定義されている OutlookItem ヘルパー クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d0f4-127">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of the current item in the inspector, before assuming the item is a contact item.</span></span>

```csharp
// This class tracks the state of an Outlook Inspector window 
// and ensures that what happens in this window is handled correctly.
class OutlookInspector
{
    // OutlookInspector class-level instance variables 
    // wrapped window object
    private Outlook.Inspector m_Window;             

    // Use these instance variables to handle item-level events
    // wrapped MailItem
    private Outlook.MailItem m_Mail;    
    // wrapped AppointmentItem        
    private Outlook.AppointmentItem m_Appointment;  
    // wrapped ContactItem
    private Outlook.ContactItem m_Contact;
    // wrapped TaskItem      
    private Outlook.TaskItem m_Task;             

    // OutlookInspector constructor
    public OutlookInspector(Outlook.Inspector inspector)
    {
        m_Window = inspector;

        // Hook up the close event
        ((Outlook.InspectorEvents_Event)inspector).Close +=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Hook up item-level events as needed
        OutlookItem olItem = new OutlookItem(inspector.CurrentItem);
        if(olItem.Class==Outlook.OlObjectClass.olContact)
        {
            m_Contact = olItem.InnerObject as Outlook.ContactItem;
            m_Contact.Open +=
                new Outlook.ItemEvents_10_OpenEventHandler(
                m_Contact_Open);
            m_Contact.PropertyChange +=
                new Outlook.ItemEvents_10_PropertyChangeEventHandler(
                m_Contact_PropertyChange);
            m_Contact.CustomPropertyChange +=
                new Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
                m_Contact_CustomPropertyChange);
        }
    }

    // Event Handler for the inspector close event.
    private void OutlookInspectorWindow_Close()
    {
        // Unhook events from any item-level instance variables
        m_Contact.Open -= 
            Outlook.ItemEvents_10_OpenEventHandler(
            m_Contact_Open);
        m_Contact.PropertyChange -= 
            Outlook.ItemEvents_10_PropertyChangeEventHandler(
            m_Contact_PropertyChange);
        m_Contact.CustomPropertyChange -= 
            Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
            m_Contact_CustomPropertyChange);
        ((Outlook.ItemEvents_Event)m_Contact).Close -= 
            Outlook.ItemEvents_CloseEventHandler(
            m_Contact_Close);

        // Unhook events from the window
        ((Outlook.InspectorEvents_Event)m_Window).Close -=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Raise the OutlookInspector close event
        if (Close != null)
        {
            Close(this, EventArgs.Empty);
        }
        // Release item-level instance variables
        m_Mail = null;
        m_Appointment = null;
        m_Contact = null;
        m_Task = null;
        m_Window = null;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3d0f4-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d0f4-128">See also</span></span>

- [<span data-ttu-id="3d0f4-129">Outlook のイベントを使用するサンプル タスク</span><span class="sxs-lookup"><span data-stu-id="3d0f4-129">Sample tasks using Outlook events</span></span>](sample-tasks-using-outlook-events.md)

