---
title: '[名前の選択] ダイアログ ボックスを表示して受信者を解決する'
TOCTitle: Display the Select Names dialog box to resolve recipients
ms:assetid: 841dd4cd-6d69-46d5-8c83-e28c95b631a9
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646055(v=office.15)
ms:contentKeyID: 55119876
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 56fb1a4abbcfca3a504315c4a0f9ba75a663aa02
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405652"
---
# <a name="display-the-select-names-dialog-box-to-resolve-recipients"></a>[名前の選択] ダイアログ ボックスを表示して受信者を解決する

この例では、*recips* パラメーターで提供された受信者の解決を試行し、あいまいで解決できない各受信者については Outlook の **[名前の選択]** ダイアログ ボックスを表示します。

## <a name="example"></a>例

次のコード サンプルでは、[SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) オブジェクトを呼び出し、[ **名前の選択**] ダイアログ ボックスに Outlook のアドレス帳を表示します。 このダイアログ ボックスを使用して、ユーザーはアドレス帳から名前を選択できます。 名前が解決されない場合は、その受信者が recips から削除されます。 名前が解決された場合、コード サンプルでは受信者の [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトを recips に返します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [受信者](recipients.md)

