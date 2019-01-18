---
title: '[名前の選択] ダイアログ ボックスを表示して受信者を解決する'
TOCTitle: Display the Select Names dialog box to resolve recipients
ms:assetid: 841dd4cd-6d69-46d5-8c83-e28c95b631a9
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646055(v=office.15)
ms:contentKeyID: 55119876
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f92891188e7c317465ce70fede1dedca7f6344fe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723041"
---
# <a name="display-the-select-names-dialog-box-to-resolve-recipients"></a><span data-ttu-id="c643e-102">[名前の選択] ダイアログ ボックスを表示して受信者を解決する</span><span class="sxs-lookup"><span data-stu-id="c643e-102">Display the Select Names dialog box to resolve recipients</span></span>

<span data-ttu-id="c643e-103">この例では、*recips* パラメーターで提供された受信者の解決を試行し、あいまいで解決できない各受信者については Outlook の **[名前の選択]** ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="c643e-103">This example attempts to resolve the recipients provided by the *recips* parameter, and displays the Outlook **Select Names** dialog box for each recipient that is ambiguous and cannot be resolved.</span></span>

## <a name="example"></a><span data-ttu-id="c643e-104">例</span><span class="sxs-lookup"><span data-stu-id="c643e-104">Example</span></span>

<span data-ttu-id="c643e-105">次のコード サンプルでは、[SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) オブジェクトを呼び出し、[ **名前の選択**] ダイアログ ボックスに Outlook のアドレス帳を表示します。</span><span class="sxs-lookup"><span data-stu-id="c643e-105">This code sample calls the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object to display the **Select Names** dialog box which shows the Outlook address book.</span></span> <span data-ttu-id="c643e-106">このダイアログ ボックスを使用して、ユーザーはアドレス帳から名前を選択できます。</span><span class="sxs-lookup"><span data-stu-id="c643e-106">Through this dialog box, the user can select a name from the address book.</span></span> <span data-ttu-id="c643e-107">名前が解決されない場合は、その受信者が recips から削除されます。</span><span class="sxs-lookup"><span data-stu-id="c643e-107">If the name is not resolved, the recipient will be removed from recips.</span></span> <span data-ttu-id="c643e-108">名前が解決された場合、コード サンプルでは受信者の [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトを recips に返します。</span><span class="sxs-lookup"><span data-stu-id="c643e-108">If the name is resolved, then the code sample will return the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object of the recipient to recips.</span></span>

<span data-ttu-id="c643e-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c643e-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c643e-110">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c643e-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c643e-111">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c643e-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ResolveRecipients(ByVal recips As Outlook.Recipients)
    If recips Is Nothing Then
        Throw New ArgumentNullException()
    End If
    If recips.ResolveAll() Then
        Return
    Else
        For i As Integer = recips.Count To 1 Step -1
            If Not (recips(i).Resolve()) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.Recipients.Add(recips(i).Name)
                snd.NumberOfRecipientSelectors = _
                    Outlook.OlRecipientSelectors.olShowTo
                snd.AllowMultipleSelection = False
                snd.Display()
                If Not (snd.Recipients.ResolveAll()) Then
                    recips.Remove(i)
                Else
                    recips.Remove(i)
                    recips.Add(snd.Recipients(1).Address)
                End If
                snd = Nothing
            End If
        Next
    End If
End Sub
```


```csharp
private void ResolveRecipients(Outlook.Recipients recips)
{
    if (recips == null)
    {
        throw new ArgumentNullException();
    }
    if (recips.ResolveAll())
    {
        return;
    }
    else
    {
        for (int i = recips.Count; i > 0; i--)
        {
            if (!recips[i].Resolve())
            {
                Outlook.SelectNamesDialog snd =
                    Application.Session.
                    GetSelectNamesDialog();
                snd.Recipients.Add(recips[i].Name);
                snd.NumberOfRecipientSelectors =
                    Outlook.OlRecipientSelectors.olShowTo;
                snd.AllowMultipleSelection = false;
                snd.Display();
                if (!snd.Recipients.ResolveAll())
                {
                    recips.Remove(i);
                }
                else
                {
                    recips.Remove(i);
                    recips.Add(snd.Recipients[1].Address);
                }
                snd = null;
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c643e-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="c643e-112">See also</span></span>

- [<span data-ttu-id="c643e-113">受信者</span><span class="sxs-lookup"><span data-stu-id="c643e-113">Recipients</span></span>](recipients.md)

