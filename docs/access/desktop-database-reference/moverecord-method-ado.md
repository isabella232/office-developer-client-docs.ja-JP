---
title: MoveRecord メソッド (ADO)
TOCTitle: MoveRecord Method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd7496efe7c38fcd78800ad087730bb21a19c32e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477794"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="bd74c-102">MoveRecord メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd74c-102">MoveRecord Method (ADO)</span></span>


<span data-ttu-id="bd74c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd74c-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="bd74c-104">[Record](record-object-ado.md) で表されるエンティティを別の場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="bd74c-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd74c-105">構文</span><span class="sxs-lookup"><span data-stu-id="bd74c-105">Syntax</span></span>

<span data-ttu-id="bd74c-106">*レコード*です。関係 (*ソース*、*変換先*、*ユーザー名*、*パスワード*、*オプション*、*非同期*)</span><span class="sxs-lookup"><span data-stu-id="bd74c-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="bd74c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bd74c-107">Parameters</span></span>

  - <span data-ttu-id="bd74c-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="bd74c-108">*Source*</span></span>

  - <span data-ttu-id="bd74c-p101">省略可能です。移動する **Record** を示す URL を含む文字列型 (**String**) の値を指定します。*Source* を省略するか、または空文字列を指定すると、この **Record** で表されるオブジェクトが移動されます。たとえば、**Record** がファイルを表している場合は、ファイルの内容が *Destination* で指定した場所に移動されます。</span><span class="sxs-lookup"><span data-stu-id="bd74c-p101">Optional. A **String** value that contains a URL identifying the **Record** to be moved. If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved. For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>

  - <span data-ttu-id="bd74c-113">*Destination*</span><span class="sxs-lookup"><span data-stu-id="bd74c-113">*Destination*</span></span>

  - <span data-ttu-id="bd74c-114">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="bd74c-114">Optional.</span></span> <span data-ttu-id="bd74c-115">*ソース*の移動先の場所を指定する URL を含む**文字列**値。</span><span class="sxs-lookup"><span data-stu-id="bd74c-115">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>

  - <span data-ttu-id="bd74c-116">*UserName*</span><span class="sxs-lookup"><span data-stu-id="bd74c-116">*UserName*</span></span>

  - <span data-ttu-id="bd74c-p103">省略可能です。*Destination* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd74c-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="bd74c-119">*Password*</span><span class="sxs-lookup"><span data-stu-id="bd74c-119">*Password*</span></span>

  - <span data-ttu-id="bd74c-p104">省略可能です。*UserName* を確認するためのパスワードを含む、文字列型 (**String**) を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd74c-p104">Optional. A **String** that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="bd74c-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="bd74c-122">*Options*</span></span>

  - <span data-ttu-id="bd74c-p105">省略可能です。[MoveRecordOptionsEnum](moverecordoptionsenum.md) 値を指定します。既定値は、 **adMoveUnspecified** です。このメソッドの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd74c-p105">Optional. A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="bd74c-126">*Async*</span><span class="sxs-lookup"><span data-stu-id="bd74c-126">*Async*</span></span>

  - <span data-ttu-id="bd74c-p106">省略可能です。ブール型 ( **Boolean** ) の値を指定します。値が **True** の場合、この動作は非同期で実行されます。</span><span class="sxs-lookup"><span data-stu-id="bd74c-p106">Optional. A **Boolean** value that, when **True**, specifies this operation should be asynchronous .</span></span>

## <a name="return-value"></a><span data-ttu-id="bd74c-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="bd74c-129">Return Value</span></span>

<span data-ttu-id="bd74c-130">文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="bd74c-130">A **String** value.</span></span> <span data-ttu-id="bd74c-131">通常、*送信先*の値が返されます。</span><span class="sxs-lookup"><span data-stu-id="bd74c-131">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="bd74c-132">ただし、実際に返される値はプロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="bd74c-132">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd74c-133">解説</span><span class="sxs-lookup"><span data-stu-id="bd74c-133">Remarks</span></span>

<span data-ttu-id="bd74c-134">*送信元*と*送信先*の値いない必要があります同じです。それ以外の場合、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bd74c-134">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="bd74c-135">少なくともサーバー、パス、およびリソース名は異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd74c-135">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="bd74c-p109">Internet Publishing Provider を使用して移動されるファイルでは、*Options* で特に指定のない限り、移動されるファイル内のすべてのハイパーテキスト リンクが更新されます。*Destination* に既存のオブジェクト (たとえば、ファイルまたはディレクトリ) を指定する場合、**adMoveOverWrite** が指定されていないと、このメソッドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="bd74c-p109">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*. This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bd74c-p110">[!メモ] <STRONG>adMoveOverWrite</STRONG> オプションは十分に注意して使用してください。たとえば、ファイルをディレクトリに移動するときにこのオプションを指定していると、移動先のディレクトリが "削除" され、移動元のファイルに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="bd74c-p110">Use the <STRONG>adMoveOverWrite</STRONG> option judiciously. For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span></P>



<span data-ttu-id="bd74c-p111">この操作の終了後、 **Record** オブジェクトの一部の属性 ( [ParentURL](parenturl-property-ado.md) プロパティなど) は更新されなくなります。 **Record** オブジェクトのプロパティを更新するには、 **Record** を閉じ、そのファイルまたはディレクトリが移動された場所の URL でもう一度開いてください。</span><span class="sxs-lookup"><span data-stu-id="bd74c-p111">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="bd74c-p112">**Recordset** から取得した [Record](recordset-object-ado.md) の場合、ファイルまたはディレクトリの移動後の場所は、 **Recordset** にすぐには反映されません。反映するには、 **Recordset** をいったん閉じてもう一度開いてください。</span><span class="sxs-lookup"><span data-stu-id="bd74c-p112">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**. Refresh the **Recordset** by closing and re-opening it.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bd74c-p113">[!メモ] http 体系を使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd74c-p113">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>

