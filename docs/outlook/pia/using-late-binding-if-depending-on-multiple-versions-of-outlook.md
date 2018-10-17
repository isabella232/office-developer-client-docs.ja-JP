---
title: 複数のバージョンの Outlook を使用する場合の遅延バインディングの使用
TOCTitle: Using late binding if depending on multiple versions of Outlook
ms:assetid: 4e5412a0-d0f8-4819-ba0f-f36ba885f8f6
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610234(v=office.15)
ms:contentKeyID: 55119791
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 866faab04e8fcac1d91b233f801f05c023ac2164
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407073"
---
# <a name="using-late-binding-if-depending-on-multiple-versions-of-outlook"></a><span data-ttu-id="89a73-102">複数のバージョンの Outlook を使用する場合の遅延バインディングの使用</span><span class="sxs-lookup"><span data-stu-id="89a73-102">Using Late Binding If Depending on Multiple Versions of Outlook</span></span>

<span data-ttu-id="89a73-103">Outlook プライマリ相互運用機能アセンブリ (PIA) を使用するマネージ Outlook アドインは、PIA が提供する型情報でコンパイルされます。</span><span class="sxs-lookup"><span data-stu-id="89a73-103">Managed Outlook add-ins that use the Outlook Primary Interop Assembly (PIA) are compiled with type information that the PIA provides.</span></span> <span data-ttu-id="89a73-104">このメソッドとプロパティに関する型情報の**事前バインド**により、コンパイラで型と構文のチェックを実行できるようになり、メソッドやプロパティに渡されるパラメーターの数と型に間違いがないことと、期待された型の値が返されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="89a73-104">This early binding of type information for methods and properties allows the compiler to perform type and syntax checks to ensure that the correct number and type of parameters are passed to the method or property, and that the returned value is of the expected type.</span></span> 

<span data-ttu-id="89a73-105">ただし、事前バインディングには、アドインが呼び出すメソッドまたはプロパティが、以前のバージョンの異なる宣言を持っている場合、バージョン間の互換性がないという欠点があります。</span><span class="sxs-lookup"><span data-stu-id="89a73-105">However, early binding has the disadvantage of introducing version incompatibility if a method or property that the add-in calls has a different declaration in an earlier version.</span></span> <span data-ttu-id="89a73-106">たとえば、新しいメソッドおよびプロパティを追加する、または既存のオブジェクトのメンバーを変更すると、オブジェクトのバイナリ レイアウトが変更され、より新しい型情報を使用して以前のバージョンの Outlook を自動化するマネージ アドインで問題が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="89a73-106">For example, adding new methods and properties or modifying existing members of an object can alter the binary layout of the object and cause problems with a managed add-in that uses the more recent type information to automate an earlier version of Outlook.</span></span> 

<span data-ttu-id="89a73-107">そのような場合、**遅延バインド**では、実行時まで待機してからオブジェクトにプロパティとメソッドの呼出しをバインドします。</span><span class="sxs-lookup"><span data-stu-id="89a73-107">In such cases, late binding waits until run time to bind property and method calls to their objects.</span></span> <span data-ttu-id="89a73-108">遅延バインディングは、Outlook のさまざまなバージョンで異なる型による混乱を防ぐことができ、複数のバージョンの Outlook を使用するアドインを記述するときに特に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="89a73-108">Late binding can help avoid complications from types that are different in different versions of Outlook, and is especially useful when writing add-ins that depend on multiple versions of Outlook.</span></span>

<span data-ttu-id="89a73-109">遅延バインドには、Outlook によって実装される [IDispatch](https://docs.microsoft.com/windows/desktop/api/oaidl/nn-oaidl-idispatch) インターフェイスを呼び出すアドインが必要になります。</span><span class="sxs-lookup"><span data-stu-id="89a73-109">Late binding involves an add-in calling the [IDispatch](https://docs.microsoft.com/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface implemented by Outlook.</span></span> <span data-ttu-id="89a73-110">Visual C\# で遅延バインドを使用する場合は、[System.Type.InvokeMember](https://docs.microsoft.com/dotnet/api/system.type.invokemember?view=netframework-4.7.2) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="89a73-110">To use late binding in Visual C#, use the [System.Type.InvokeMember](https://docs.microsoft.com/dotnet/api/system.type.invokemember?view=netframework-4.7.2) method.</span></span> <span data-ttu-id="89a73-111">このメソッドは、[IDispatch::GetIDsOfNames](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) と [IDispatch::Invoke](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) を呼び出して、Outlook のメソッドとプロパティをバインドします。</span><span class="sxs-lookup"><span data-stu-id="89a73-111">This method calls [IDispatch::GetIDsOfNames](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [IDispatch::Invoke](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to bind to Outlook's methods and properties.</span></span> <span data-ttu-id="89a73-112">IDispatch::GetIDsOfNames メソッドを使用すると、Visual C\# で、オブジェクトがサポートしているメソッドとプロパティについてオブジェクトを照会できます。それらのメソッドとプロパティは、IDispatch::Invoke メソッドを使用すると Visual C\# で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="89a73-112">The \# method allows Visual C# to interrogate an object about what methods and properties it supports and the \# method then allows Visual C# to call those methods and properties.</span></span> 

<!-- PAGES 404 
For more information about using late binding in C\#, see [KB 302902: Binding for Office Automation Servers with Visual C\# .NET](https://go.microsoft.com/fwlink/?linkid=88971). For more information about using late binding in Visual Basic, see [KB 304661: How to Use Visual Basic .NET for Binding for Office Automation Servers](https://go.microsoft.com/fwlink/?linkid=88972).

Note that late binding requires obtaining a DispID for every method or property, so late binding generally does not perform as well as early binding. For more information about how early binding compares with late binding, see [KB 245115: Using Early Binding and Late Binding in Automation](https://go.microsoft.com/fwlink/?linkid=88973). -->

## <a name="see-also"></a><span data-ttu-id="89a73-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="89a73-113">See also</span></span>

- [<span data-ttu-id="89a73-114">COM と .NET の相互運用性の概要</span><span class="sxs-lookup"><span data-stu-id="89a73-114">Introduction to Interoperability Between COM and .NET</span></span>](introduction-to-interoperability-between-com-and-net.md)
