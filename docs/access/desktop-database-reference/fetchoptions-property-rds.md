---
title: FetchOptions プロパティ (RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 60eb05d87e7d31d283cdcf29c0f6240892fe29ef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477622"
---
# <a name="fetchoptions-property-rds"></a><span data-ttu-id="604fe-102">FetchOptions プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="604fe-102">FetchOptions Property (RDS)</span></span>


<span data-ttu-id="604fe-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="604fe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="604fe-104">非同期フェッチの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="604fe-104">Indicates the type of asynchronous fetching.</span></span>

## <a name="setting-and-return-values"></a><span data-ttu-id="604fe-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="604fe-105">Setting and Return Values</span></span>

<span data-ttu-id="604fe-106">次のいずれかの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="604fe-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="604fe-107">定数</span><span class="sxs-lookup"><span data-stu-id="604fe-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="604fe-108">説明</span><span class="sxs-lookup"><span data-stu-id="604fe-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="604fe-109"><strong>adcFetchUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="604fe-109"><strong>adcFetchUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="604fe-p101">Recordset のすべてのレコードは、制御がアプリケーションに返される前にフェッチされます。アプリケーションで Recordset を操作できるように、事前に Recordset 全体がフェッチされます。</span><span class="sxs-lookup"><span data-stu-id="604fe-p101">All the records of the <a href="recordset-object-ado.md">Recordset</a> are fetched before control is returned to the application. The complete <strong>Recordset</strong> is fetched before the application is allowed to do anything with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604fe-112"><strong>adcFetchBackground</strong></span><span class="sxs-lookup"><span data-stu-id="604fe-112"><strong>adcFetchBackground</strong></span></span></p></td>
<td><p><span data-ttu-id="604fe-p102">レコードの最初のバッチがフェッチされると、制御をアプリケーションに戻すことができます。最初のバッチでフェッチされなかったレコードへのアクセスを試みるそれ以降の <strong>Recordset</strong> の読み取りは、要求されたレコードが実際にフェッチされて制御がアプリケーションに戻るまで遅延されます。</span><span class="sxs-lookup"><span data-stu-id="604fe-p102">Control can return to the application as soon as the first batch of records has been fetched. A subsequent read of the <strong>Recordset</strong> that attempts to access a record not fetched in the first batch will be delayed until the sought record is actually fetched, at which time control returns to the application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604fe-115"><strong>adcFetchAsync</strong></span><span class="sxs-lookup"><span data-stu-id="604fe-115"><strong>adcFetchAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="604fe-p103">既定値です。レコードがバックグラウンドでフェッチされる間に、制御は直ちにアプリケーションに戻ります。フェッチされていないレコードをアプリケーションが読み取ろうとした場合、要求されているレコードに最も近いレコードが読み取られ、制御はすぐに戻り、現在の <strong>Recordset</strong> の最終位置に到達したことを示します。たとえば、<a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> を呼び出した場合、現在のレコードの位置は、<strong>Recordset</strong> にさらに多くのレコードが格納される予定であっても、実際にフェッチされた最後のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="604fe-p103">Default. Control returns immediately to the application while records are fetched in the background. If the application attempts to read a record that hasn't yet been fetched, the record closest to the sought record will be read and control will return immediately, indicating that the current end of the <strong>Recordset</strong> has been reached. For example, a call to <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> will move the current record position to the last record actually fetched, even though more records will continue to populate the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="604fe-p104">[!メモ] これらの定数を使用するクライアント側の各実行可能ファイルで、使用する定数を宣言する必要があります。定数の宣言は、C:\Program Files\Common Files\System\MSADC フォルダーにある Adcvbs.inc ファイルからコピーして貼り付けることができます。</span><span class="sxs-lookup"><span data-stu-id="604fe-p104">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="604fe-122">解説</span><span class="sxs-lookup"><span data-stu-id="604fe-122">Remarks</span></span>

<span data-ttu-id="604fe-p105">Web アプリケーションでは、より高いパフォーマンスを得るため、一般に **adcFetchAsync** (既定値) を使います。コンパイルされたクライアント アプリケーションでは、一般に **adcFetchBackground** を使います。</span><span class="sxs-lookup"><span data-stu-id="604fe-p105">In a Web application, you will usually want to use **adcFetchAsync** (the default value), because it provides better performance. In a compiled client application, you will usually want to use **adcFetchBackground**.</span></span>
