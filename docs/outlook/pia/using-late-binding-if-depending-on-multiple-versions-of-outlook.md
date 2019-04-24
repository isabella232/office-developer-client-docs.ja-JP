---
title: 複数のバージョンの Outlook を使用する場合の遅延バインディングの使用
TOCTitle: Using late binding if depending on multiple versions of Outlook
ms:assetid: 4e5412a0-d0f8-4819-ba0f-f36ba885f8f6
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610234(v=office.15)
ms:contentKeyID: 55119791
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4cca4d426e5e7e9fd06fa3a0c3af1158b7e6c2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357471"
---
# <a name="using-late-binding-if-depending-on-multiple-versions-of-outlook"></a>複数のバージョンの Outlook を使用する場合の遅延バインディングの使用

Outlook プライマリ相互運用機能アセンブリ (PIA) を使用するマネージ Outlook アドインは、PIA が提供する型情報でコンパイルされます。 このメソッドとプロパティに関する型情報の**事前バインド**により、コンパイラで型と構文のチェックを実行できるようになり、メソッドやプロパティに渡されるパラメーターの数と型に間違いがないことと、期待された型の値が返されることが保証されます。 

ただし、事前バインディングには、アドインが呼び出すメソッドまたはプロパティが、以前のバージョンの異なる宣言を持っている場合、バージョン間の互換性がないという欠点があります。 たとえば、新しいメソッドおよびプロパティを追加する、または既存のオブジェクトのメンバーを変更すると、オブジェクトのバイナリ レイアウトが変更され、より新しい型情報を使用して以前のバージョンの Outlook を自動化するマネージ アドインで問題が発生する場合があります。 

そのような場合、**遅延バインド**では、実行時まで待機してからオブジェクトにプロパティとメソッドの呼出しをバインドします。 遅延バインディングは、Outlook のさまざまなバージョンで異なる型による混乱を防ぐことができ、複数のバージョンの Outlook を使用するアドインを記述するときに特に役立ちます。

遅延バインドには、Outlook によって実装される [IDispatch](https://docs.microsoft.com/windows/desktop/api/oaidl/nn-oaidl-idispatch) インターフェイスを呼び出すアドインが必要になります。 Visual C\# で遅延バインドを使用する場合は、[System.Type.InvokeMember](https://docs.microsoft.com/dotnet/api/system.type.invokemember?view=netframework-4.7.2) メソッドを使用します。 このメソッドは、[IDispatch::GetIDsOfNames](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) と [IDispatch::Invoke](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) を呼び出して、Outlook のメソッドとプロパティをバインドします。 IDispatch::GetIDsOfNames メソッドを使用すると、Visual C\# で、オブジェクトがサポートしているメソッドとプロパティについてオブジェクトを照会できます。それらのメソッドとプロパティは、IDispatch::Invoke メソッドを使用すると Visual C\# で呼び出すことができます。 

<!-- PAGES 404 
For more information about using late binding in C\#, see [KB 302902: Binding for Office Automation Servers with Visual C\# .NET](https://go.microsoft.com/fwlink/?linkid=88971). For more information about using late binding in Visual Basic, see [KB 304661: How to Use Visual Basic .NET for Binding for Office Automation Servers](https://go.microsoft.com/fwlink/?linkid=88972).

Note that late binding requires obtaining a DispID for every method or property, so late binding generally does not perform as well as early binding. For more information about how early binding compares with late binding, see [KB 245115: Using Early Binding and Late Binding in Automation](https://go.microsoft.com/fwlink/?linkid=88973). -->

## <a name="see-also"></a>関連項目

- [COM と .NET の相互運用性の概要](introduction-to-interoperability-between-com-and-net.md)

