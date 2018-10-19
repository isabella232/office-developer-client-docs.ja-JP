---
title: Outlook のインスタンスを取得し、サインインする
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462097(v=office.15)
ms:contentKeyID: 55119926
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 6aa4ecb0b6d9a3082759c7a3b0b4a5f677d1556e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406464"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a>Outlook のインスタンスを取得し、サインインする

このトピックでは、ローカル コンピューターで Microsoft Outlook が実行されている場合には Outlook のアクティブ インスタンスを表す [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクトを取得し、そうでない場合には Outlook の新しいインスタンスを作成し、既定のプロファイルにサインインし、Outlook のそのインスタンスを返す方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、Helmut Obertanner 氏が提供したものです。 Helmut 氏の得意分野は、Office Developer Tools for Visual Studio と Outlook です。 

次のコード例には、Sample クラスの GetApplicationObject メソッドが含まれています。このメソッドは、Outlook アドイン プロジェクトの一部として実装されています。 それぞれのプロジェクトでは、[Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) 名前空間に基づいた、Outlook プライマリ互換運用機能アセンブリへの参照を追加しています。

GetApplicationObject メソッドは、.NET Framework クラス ライブラリのクラスを使用して、ローカル コンピューターで実行中の Outlook プロセスを確認および取得します。 まず、 [System.Diagnostics](https://msdn.microsoft.com/ja-JP/library/wbt7d3cy) 名前空間内の [Process](https://msdn.microsoft.com/ja-JP/library/ccf1tfx0) クラスの [GetProcessesByName](https://msdn.microsoft.com/ja-JP/library/15t15zda) メソッドを使用して、ローカル コンピューター上のプロセス名 "OUTLOOK" のプロセス コンポーネントの配列を取得します。 配列に少なくとも 1 つの Outlook プロセスが含まれているかどうかを確認するために、GetApplicationObject では Microsoft 統合言語クエリ (LINQ) を使用しています。 [System.Linq](https://msdn.microsoft.com/ja-JP/library/bb345746) 名前空間内の [Enumerable](https://msdn.microsoft.com/ja-JP/library/bb336768) クラスには、 \> ジェネリック インターフェイスを実装している各種メソッドがあり、 [Count](https://msdn.microsoft.com/ja-JP/library/9eekhta0) メソッドもその 1 つです。 [Array](https://msdn.microsoft.com/ja-JP/library/czz5hkty) クラスは **IEnumerable(T)** インターフェイスを実装しているため、**GetProcessesByName** から返された配列に **Count** メソッドを利用することで、実行中の Outlook プロセスが存在するかどうかを確認できます。 存在している場合、GetApplicationObject は [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) 名前空間の [Marshal](https://msdn.microsoft.com/ja-JP/library/asx0thw2) クラスに含まれる [GetActiveObject](https://msdn.microsoft.com/ja-JP/library/xt620x09) メソッドを使用して、その Outlook のインスタンスを取得し、そのオブジェクトを Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクトにキャストします。

Outlook がローカル コンピューターで実行中ではない場合、GetApplicationObject では、Outlook の新しいインスタンスを作成し、[NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [Logon(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb646718\(v=office.15\)) メソッドを使用して既定のプロファイルにサインインし、Outlook のその新しいインスタンスを返します。

次に、Visual Basic のコード例を示します。その後に、C\# のコード例を示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports System.Diagnostics
Imports System.Linq
Imports System.Reflection
Imports System.Runtime.InteropServices
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample

        Function GetApplicationObject() As Outlook.Application

            Dim application As Outlook.Application

            ' Check whether there is an Outlook process running.
            If Process.GetProcessesByName("OUTLOOK").Count() > 0 Then

                ' If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = DirectCast(Marshal.GetActiveObject("Outlook.Application"), Outlook.Application)
            Else

                ' If not, create a new instance of Outlook and sign in to the default profile.
                application = New Outlook.Application()
                Dim ns As Outlook.NameSpace = application.GetNamespace("MAPI")
                ns.Logon("", "", Missing.Value, Missing.Value)
                ns = Nothing
            End If

            ' Return the Outlook Application object.
            Return application
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Diagnostics;
using System.Linq;
using System.Reflection;
using System.Runtime.InteropServices;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.Application GetApplicationObject()
        {

            Outlook.Application application = null;

            // Check whether there is an Outlook process running.
            if (Process.GetProcessesByName("OUTLOOK").Count() > 0)
            {

                // If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = Marshal.GetActiveObject("Outlook.Application") as Outlook.Application;
            }
            else
            {

                // If not, create a new instance of Outlook and sign in to the default profile.
                application = new Outlook.Application();
                Outlook.NameSpace nameSpace = application.GetNamespace("MAPI");
                nameSpace.Logon("", "", Missing.Value, Missing.Value);
                nameSpace = null;
            }

            // Return the Outlook Application object.
            return application;
        }

    }
}
```

## <a name="see-also"></a>関連項目

- [セッション](sessions.md)

