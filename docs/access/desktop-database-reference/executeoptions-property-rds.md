---
title: ExecuteOptions プロパティ (RDS)
TOCTitle: ExecuteOptions Property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e5a91d3941db0b7daa61b506c136dab59f24ed0
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603589"
---
# <a name="executeoptions-property-rds"></a><span data-ttu-id="2b8fc-102">ExecuteOptions プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="2b8fc-102">ExecuteOptions Property (RDS)</span></span>


<span data-ttu-id="2b8fc-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b8fc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2b8fc-104">非同期実行が有効かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="2b8fc-104">Indicates whether asynchronous execution is enabled.</span></span>

<span data-ttu-id="2b8fc-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="2b8fc-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="2b8fc-106">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="2b8fc-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="2b8fc-107">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="2b8fc-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="2b8fc-108">master</span><span class="sxs-lookup"><span data-stu-id="2b8fc-108">master</span></span>

<span data-ttu-id="2b8fc-109">次のいずれかの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="2b8fc-109">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b8fc-110">定数</span><span class="sxs-lookup"><span data-stu-id="2b8fc-110">Constant</span></span></p></th>
<th><p><span data-ttu-id="2b8fc-111">説明</span><span class="sxs-lookup"><span data-stu-id="2b8fc-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b8fc-112"><strong>adcExecSync</strong></span><span class="sxs-lookup"><span data-stu-id="2b8fc-112"><strong>adcExecSync</strong></span></span></p></td>
<td><p><span data-ttu-id="2b8fc-113">次回の <a href="recordset-object-ado.md">Recordset</a> の更新を同期的に実行します。</span><span class="sxs-lookup"><span data-stu-id="2b8fc-113">Executes the next refresh of the <a href="recordset-object-ado.md">Recordset</a> synchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b8fc-114"><strong>adcExecAsync</strong></span><span class="sxs-lookup"><span data-stu-id="2b8fc-114"><strong>adcExecAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="2b8fc-p101">既定値です。次回の <strong>Recordset</strong> の更新を非同期的に実行します。</span><span class="sxs-lookup"><span data-stu-id="2b8fc-p101">Default. Executes the next refresh of the <strong>Recordset</strong> asynchronously.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="2b8fc-p102">[!メモ] これらの定数を使うクライアント側の各実行可能ファイルは、その定数を宣言する必要があります。C:\Program Files\Common Files\System\MSADC フォルダーの Adcvbs.inc ファイルから、定数の宣言を切り取って貼り付けることができます。</span><span class="sxs-lookup"><span data-stu-id="2b8fc-p102">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations that you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="2b8fc-119">解説</span><span class="sxs-lookup"><span data-stu-id="2b8fc-119">Remarks</span></span>

<span data-ttu-id="2b8fc-120">**ExecuteOptions** が **adcExecAsync** に設定されている場合、 **RDS.DataControl** オブジェクトの [Recordset](datacontrol-object-rds.md) における次の **Refresh** 呼び出しは非同期的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="2b8fc-120">If **ExecuteOptions** is set to **adcExecAsync**, then this asynchronously executes the next **Refresh** call on the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset**.</span></span>

<span data-ttu-id="2b8fc-121">[RDS.DataControl](reset-method-rds.md) オブジェクトの [Recordset](refresh-method-rds.md) に変更を行う可能性のある別の非同期操作の実行中に [Reset](submitchanges-method-rds.md)、[Refresh](cancelupdate-method-ado.md)、[SubmitChanges](recordset-sourcerecordset-properties-rds.md)、[CancelUpdate](datacontrol-object-rds.md)、または **Recordset** を呼び出そうとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2b8fc-121">If you try to call [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md), or [Recordset](recordset-sourcerecordset-properties-rds.md) while another asynchronous operation that might change the [RDS.DataControl](datacontrol-object-rds.md) object's **Recordset** is executing, an error occurs.</span></span>

<span data-ttu-id="2b8fc-122">非同期操作中にエラーが発生した場合、**RDS.DataControl** オブジェクトの [ReadyState](readystate-property-rds.md) 値が **adcReadyStateLoaded** から **adcReadyStateComplete** に変更され、**Recordset** プロパティ値は *Nothing* のまま維持されます。</span><span class="sxs-lookup"><span data-stu-id="2b8fc-122">If an error occurs during an asynchronous operation, the **RDS.DataControl** object's [ReadyState](readystate-property-rds.md) value changes from **adcReadyStateLoaded** to **adcReadyStateComplete**, and the **Recordset** property value remains *Nothing*.</span></span>

