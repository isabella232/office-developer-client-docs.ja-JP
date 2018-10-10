---
title: '手順 3: Fields リスト ボックスに値を設定する'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca764e2339d0c866922be2982a168afc03d84c1d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476869"
---
# <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="d95a6-102">手順 3: Fields リスト ボックスに値を設定する</span><span class="sxs-lookup"><span data-stu-id="d95a6-102">Step 3: Populate the Fields List Box</span></span>


<span data-ttu-id="d95a6-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d95a6-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="d95a6-104">手順 3: Fields リスト ボックスに値を設定する</span><span class="sxs-lookup"><span data-stu-id="d95a6-104">Step 3: Populate the Fields List Box</span></span>

<span data-ttu-id="d95a6-105">**Fields リスト ボックスに値を設定するには**</span><span class="sxs-lookup"><span data-stu-id="d95a6-105">**To populate the Fields list box**</span></span>

<span data-ttu-id="d95a6-106">lstMain の Click イベント ハンドラーに次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="d95a6-106">Insert the following code into the Click event handler of lstMain:</span></span>

```vb 
 
Private Sub lstMain_Click() 
    Dim rec As Record 
    Dim rs As Recordset 
    Set rec = New Record 
    Set rs = New Recordset 
    grs.MoveFirst 
    grs.Move lstMain.ListIndex 
    lstDetails.Clear 
    rec.Open grs 
    Select Case rec.RecordType 
        Case adCollectionRecord: 
            Set rs = rec.GetChildren 
            While Not rs.EOF 
                lstDetails.AddItem rs(0) 
                rs.MoveNext 
            Wend 
        Case adSimpleRecord: 
            recFields rec, lstDetails, txtDetails 
             
        Case adStructDoc: 
    End Select 
     
End Sub 
```

<span data-ttu-id="d95a6-107">このコードを宣言し、ローカル**レコード**と**レコード セット**オブジェクト、レコードのインスタンスを作成し、rs、それぞれ。</span><span class="sxs-lookup"><span data-stu-id="d95a6-107">This code declares and instantiates local **Record** and **Recordset** objects, rec and and rs, respectively.</span></span>

<span data-ttu-id="d95a6-108">LstMain 内で選択されたリソースに対応する行には、grs の現在の行が行われます。</span><span class="sxs-lookup"><span data-stu-id="d95a6-108">The row corresponding to the resource selected in lstMain is made the current row of grs.</span></span> <span data-ttu-id="d95a6-109">**[詳細**] ボックスの一覧ボックスがオフになってとの現在の行にレコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="d95a6-109">Then the **Details** list box is cleared and rec is opened with the current row of .</span></span> <span data-ttu-id="d95a6-110">**詳細**のリスト ボックスをオフにし、およびソースとして grs の現在の行にレコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="d95a6-110">Then the **Details** list box is cleared and rec is opened with the current row of grs as the source.</span></span>

<span data-ttu-id="d95a6-111">リソースがコレクション レコード ( **RecordType**で指定) と同じである場合は、レコードの子で、ローカル**レコード セット**rs が開かれます。LstDetails の行から値を入力し、レコードの子で開かれます。[LstDetails rs の行から値が入力されます。</span><span class="sxs-lookup"><span data-stu-id="d95a6-111">If the resource is a collection record (as specified by **RecordType**), the local **Recordset**, rs, is opened on the children of rec. Then lstDetails is filled with the values from the rows of is opened on the children of rec. Then lstDetails is filled with the values from the rows of rs.</span></span>

<span data-ttu-id="d95a6-p102">リソースが単純レコードである場合は、recFields が呼び出されます。recFields の詳細については、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d95a6-p102">If the resource is a simple record, recFields is called. For more information about recFields, see the next step.</span></span>

<span data-ttu-id="d95a6-114">リソースが構造化ドキュメントである場合は、コードは実装されません。</span><span class="sxs-lookup"><span data-stu-id="d95a6-114">No code is implemented if the resource is a structured document.</span></span>

