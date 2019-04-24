---
title: Outlook PIA でのオブジェクト
TOCTitle: Objects in the Outlook PIA
ms:assetid: 1be732a6-d6da-4fa0-beaa-accf35db12d6
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609459(v=office.15)
ms:contentKeyID: 55119778
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 772d857e10068871de16c2a3cd0528ab08088631
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270252"
---
# <a name="objects-in-the-outlook-pia"></a><span data-ttu-id="cba57-102">Outlook PIA のオブジェクト</span><span class="sxs-lookup"><span data-stu-id="cba57-102">Objects in the Outlook PIA</span></span>

<span data-ttu-id="cba57-103">オブジェクト ブラウザーで Outlook プライマリ相互運用機能アセンブリ (PIA) をブラウズすると、多くのインターフェイスやクラスの名前が、Outlook オブジェクト モデルでお馴染みのオブジェクトを指していることに気付きます。</span><span class="sxs-lookup"><span data-stu-id="cba57-103">When browsing the Outlook Primary Interop Assembly (PIA) in an object browser, you may notice that many interfaces and classes have names referencing familiar objects in the Outlook object model.</span></span> <span data-ttu-id="cba57-104">このオブジェクト モデルの一部のオブジェクトには、PIA のインターフェイスに対する一対一のマッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="cba57-104">Some objects in the object model have a one-to-one mapping to interfaces in the PIA.</span></span> 

<span data-ttu-id="cba57-105">たとえば、 **AddressEntry** は [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) インターフェイスにマップされ、 **AddressList** オブジェクトは PIA の [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) インターフェイスにマップされます。</span><span class="sxs-lookup"><span data-stu-id="cba57-105">For example, the **AddressEntry** is mapped to the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) interface and the **AddressList** object is mapped to the [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) interface in the PIA.</span></span> 

<span data-ttu-id="cba57-106">しかし、その他の多くのオブジェクトには、PIA の一対多マッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="cba57-106">However, most other objects have a one-to-many mapping in the PIA.</span></span> <span data-ttu-id="cba57-107">この一対多マッピングは、Microsoft Office Outlook 2007 より以前から存在する一部のオブジェクトと、Outlook 2007 以降に追加されたすべてのオブジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="cba57-107">This one-to-many mapping applies to some objects that existed before Microsoft Office Outlook 2007, and all objects added since Outlook 2007.</span></span> <span data-ttu-id="cba57-108">このトピックでは、COM オブジェクトにマップされる典型的な .NET インターフェイス、クラス、およびデリゲートを示し、Outlook PIA のオブジェクトにアクセスする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="cba57-108">This topic lists the typical .NET interfaces, classes, and delegates that are mapped to a COM object and describes how to access an object in the Outlook PIA.</span></span> <span data-ttu-id="cba57-109">また、COM ベースのオブジェクト モデルではオブジェクトが非公開または非推奨になっている Outlook PIA のいくつかの例外についても説明します。</span><span class="sxs-lookup"><span data-stu-id="cba57-109">It also describes a few exceptions in the Outlook PIA where the objects are hidden or deprecated in the COM-based object model.</span></span>

## <a name="helper-objects"></a><span data-ttu-id="cba57-110">ヘルパー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="cba57-110">Helper objects</span></span>

<span data-ttu-id="cba57-p103">このセクションでは、 **FormRegion** オブジェクトを例として使用し、Outlook PIA のオブジェクトに対する典型的なヘルパー クラスを示します。 **FormRegion** オブジェクトがオブジェクト モデルに追加されたのは Outlook 2007 のときです。PIA の **FormRegion** オブジェクトに関連するものには、図 1 に示すインターフェイス、クラス、およびデリゲートがあります。</span><span class="sxs-lookup"><span data-stu-id="cba57-p103">This section illustrates the typical helper classes for an object in the Outlook PIA by using the **FormRegion** object as an example. The **FormRegion** object was added to the object model in Outlook 2007. Related to the **FormRegion** object in the PIA are the interfaces, classes, and delegates, illustrated in Figure 1.</span></span>

<span data-ttu-id="cba57-114">**図 1. Outlook オブジェクト モデルと Outlook PIA での FormRegion オブジェクトの表現**</span><span class="sxs-lookup"><span data-stu-id="cba57-114">**Figure 1. The FormRegion object represented in the Outlook object model and in the Outlook PIA**</span></span>

![Outlook オブジェクト モデルと Outlook PIA での FormRegion オブジェクトの表現](media/pia-outlook-object-model.gif)

<span data-ttu-id="cba57-116">**FormRegion** オブジェクトとそのメソッド、プロパティ、およびイベント メンバーへのアクセスに最も頻繁に使用するインターフェイスが、[FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)) インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="cba57-116">The one interface that you most often use to access the **FormRegion** object and its method, property, and event members is the [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\)) interface.</span></span> <span data-ttu-id="cba57-117">ただし、**FormRegion** .NET インターフェイスは **FormRegion** COM オブジェクトの完全なミラー イメージであると見なすことはできません。Visual Studio のオブジェクト ブラウザーで調べると、**FormRegion** インターフェイスは別のインターフェイスである [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)) インターフェイスから継承していることがわかります。</span><span class="sxs-lookup"><span data-stu-id="cba57-117">However, you should not consider the **FormRegion** .NET interface as an exact mirror image of the **FormRegion** COM object; if you look at the Object Browser in Visual Studio, you will find that the **FormRegion** interface inherits from another interface, the [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)) interface.</span></span> <span data-ttu-id="cba57-118">実際、**FormRegion** インターフェイスは、COM タイプ ライブラリに基づいて Outlook PIA を作成した結果による、いくつかのインターフェイスとクラスのうちの 1 つに過ぎません。</span><span class="sxs-lookup"><span data-stu-id="cba57-118">In fact, the **FormRegion** interface is just one of the few interfaces and classes that result from creating the Outlook PIA based on the COM type library.</span></span>

<span data-ttu-id="cba57-p105">Outlook は、Outlook PIA を作成するために .NET Framework のタイプ ライブラリ インポーター (TLBIMP) を使用して COM タイプ ライブラリのタイプの定義を共通言語ランタイム アセンブリの同等の定義に変換します。COM における **FormRegion** オブジェクトは、実際には、 **FormRegion** オブジェクトで実装されるインターフェイスを定義する次の 2 つのインターフェイスから成るコクラスとなります。</span><span class="sxs-lookup"><span data-stu-id="cba57-p105">To create the Outlook PIA, Outlook uses the Type Library Importer (TLBIMP) in the .NET Framework to convert type definitions in the COM type library into equivalent definitions in a Common Language Runtime assembly. In COM, the **FormRegion** object is actually a coclass that consists of the following two interfaces defining the interfaces that the **FormRegion** object implements:</span></span>

- <span data-ttu-id="cba57-121">プライマリ インターフェイス **\_FormRegion**</span><span class="sxs-lookup"><span data-stu-id="cba57-121">The primary interface **\_FormRegion**</span></span>

- <span data-ttu-id="cba57-122">イベント インターフェイス [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="cba57-122">The event interface [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))</span></span>

<span data-ttu-id="cba57-123">TLBIMP は、タイプ ライブラリから **\_FormRegion** と **FormRegionEvents** を直接インポートします。</span><span class="sxs-lookup"><span data-stu-id="cba57-123">TLBIMP directly imports **\_FormRegion** and **FormRegionEvents** from the type library.</span></span>

<span data-ttu-id="cba57-p106">TLBIMP は、プライマリ インターフェイスとイベント インターフェイスをインポートするだけでなく、COM オブジェクトと同じ名前の .NET インターフェイスと .NET クラスを作成します。このクラスの名前はオブジェクト名に "Class" を付けたものとなります。 **FormRegion** オブジェクトの場合は、TLBIMP によって次のものが作成されます。</span><span class="sxs-lookup"><span data-stu-id="cba57-p106">Other than importing the primary interface and event interface, TLBIMP creates a .NET interface that has the same name as the COM object, and a .NET class that uses the name of the object and appends it with "Class". In the case of the **FormRegion** object, TLBIMP creates the following:</span></span>

- <span data-ttu-id="cba57-126">.NET インターフェイス **FormRegion**</span><span class="sxs-lookup"><span data-stu-id="cba57-126">The .NET interface **FormRegion**</span></span>

- <span data-ttu-id="cba57-127">.NET クラス [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="cba57-127">The .NET class [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\))</span></span>

<span data-ttu-id="cba57-p107">このトピックで説明する .NET インターフェイスと .NET クラスに関しては、必ず TLBIMP で作成した .NET インターフェイスを使用してオブジェクトにアクセスします。たとえば、VB の **FormRegion** オブジェクトにアクセスするには、次のコード例で示すように、必ず **FormRegion** インターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="cba57-p107">Of the .NET interfaces and .NET class mentioned in this topic, you always use the .NET interface that TLBIMP creates to access an object. For example, to access a **FormRegion** object in VB, you always use the **FormRegion** interface, as in the following code example:</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
Sub DemoFormRegion(ByVal Region As Outlook.FormRegion)
    Dim MyFormRegion As Outlook.FormRegion = Region
    ' Additional method code here
End Sub
```

<br/>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook; 
void DemoFormRegion(Outlook.FormRegion region) 
{
    Outlook.FormRegion myFormRegion = region; 
    // Additional method code here
}
```

<span data-ttu-id="cba57-130">TLBIMP でインポートされるプライマリ インターフェイスと作成される .NET クラスの詳細については、「[Outlook PIA でのメソッドとプロパティ](methods-and-properties-in-the-outlook-pia.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cba57-130">For information about the purpose of the primary interface and the .NET class that TLBIMP imports and creates respectively, see [Methods and properties in the Outlook PIA](methods-and-properties-in-the-outlook-pia.md).</span></span> <span data-ttu-id="cba57-131">イベントに関連するインターフェイスの用途の詳細については、「[Outlook PIA でのイベント](events-in-the-outlook-pia.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cba57-131">For information about the purpose of the event-related interfaces, delegates, and sink helper classes, see [Events in the Outlook PIA](events-in-the-outlook-pia.md).</span></span>

## <a name="deprecated-objects"></a><span data-ttu-id="cba57-132">非推奨オブジェクト</span><span class="sxs-lookup"><span data-stu-id="cba57-132">Deprecated objects</span></span>

<span data-ttu-id="cba57-133">タイプ ライブラリでは非推奨のオブジェクトが、Outlook PIA では公開されています。</span><span class="sxs-lookup"><span data-stu-id="cba57-133">Objects deprecated in the type library are exposed in the Outlook PIA.</span></span> <span data-ttu-id="cba57-134">たとえば、タイプ ライブラリでは **\_DDocSiteControl** オブジェクトと **\_DRecipientControl** オブジェクトは非公開になっていますが、PIA では公開されています。</span><span class="sxs-lookup"><span data-stu-id="cba57-134">For example, the **\_DDocSiteControl** and **\_DRecipientControl** objects are hidden in the type library but are exposed in the PIA.</span></span>

<span data-ttu-id="cba57-135">非推奨オブジェクトのもう 1 つの例として、**MAPIFolder** オブジェクトが挙げられます。</span><span class="sxs-lookup"><span data-stu-id="cba57-135">Another example of a deprecated object is the **MAPIFolder** object.</span></span> <span data-ttu-id="cba57-136">Outlook 2007 以降のオブジェクト モデルでは、 **MAPIFolder** オブジェクトに代わって **Folder** オブジェクトを使用することになりました。</span><span class="sxs-lookup"><span data-stu-id="cba57-136">Starting in Outlook 2007, the **Folder** object has replaced the **MAPIFolder** object in the object model.</span></span> <span data-ttu-id="cba57-137">既存のソリューションが **MAPIFolder** を参照している場合はそれを **Folder** に変更し、Outlook 2007 以降の新しいソリューションでは、常に **Folder** オブジェクトだけを使用するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="cba57-137">Existing solutions should replace references to **MAPIFolder** by **Folder**, and all solutions new for Outlook 2007 and after should use only the **Folder** object.</span></span> <span data-ttu-id="cba57-138">非管理対象のソリューションの場合、 **MAPIFolder** オブジェクトは、Visual Basic Editor のオブジェクト ブラウザーで隠しオブジェクトとしてもリストされません。</span><span class="sxs-lookup"><span data-stu-id="cba57-138">For unmanaged solutions, the Object Browser of the Visual Basic Editor no longer lists the **MAPIFolder** object, not even as a hidden object.</span></span> 

<span data-ttu-id="cba57-139">管理対象のソリューションの場合、Outlook PIA では、 [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトとそのメンバーにアクセスするための **Folder** インターフェイスが公開されますが、 [Folder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) オブジェクトのメンバーを定義するインターフェイスとして **MAPIFolder** も公開されます。</span><span class="sxs-lookup"><span data-stu-id="cba57-139">For managed solutions, even though the Outlook PIA exposes a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) interface through which you access the **Folder** object and its members, the Outlook PIA also exposes [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) as an interface that defines the members of the **Folder** object.</span></span>

## <a name="see-also"></a><span data-ttu-id="cba57-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="cba57-140">See also</span></span>

- [<span data-ttu-id="cba57-141">Outlook PIA とオブジェクト モデルの関係</span><span class="sxs-lookup"><span data-stu-id="cba57-141">Relating the Outlook PIA with the object model</span></span>](relating-the-outlook-pia-with-the-object-model.md)


