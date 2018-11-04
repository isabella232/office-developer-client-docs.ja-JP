---
title: CopyRecord メソッド (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 161cfec0e8450ef7e80c47bc8fb1b8304790e7c5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949909"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="1f975-102">CopyRecord メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="1f975-102">CopyRecord method (ADO)</span></span>

<span data-ttu-id="1f975-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1f975-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f975-104">**Record** で表されるエンティティを別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="1f975-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f975-105">構文</span><span class="sxs-lookup"><span data-stu-id="1f975-105">Syntax</span></span>

<span data-ttu-id="1f975-106">*レコード*です。定義 (*ソース*、*変換先*、*ユーザー名*、*パスワード*、*オプション*、*非同期*)</span><span class="sxs-lookup"><span data-stu-id="1f975-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="1f975-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1f975-107">Parameters</span></span>

|<span data-ttu-id="1f975-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1f975-108">Parameter</span></span>|<span data-ttu-id="1f975-109">説明</span><span class="sxs-lookup"><span data-stu-id="1f975-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1f975-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="1f975-110">*Source*</span></span> |<span data-ttu-id="1f975-111">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="1f975-111">Optional.</span></span> <span data-ttu-id="1f975-112">コピー元のエンティティ (ファイル、ディレクトリなど) を指定する URL を含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1f975-112">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="1f975-113">*ソース*を省略すると、空の文字列を指定する場合は、ファイルまたはディレクトリが現在の[レコード](record-object-ado.md)で表されますがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="1f975-113">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>|
|<span data-ttu-id="1f975-114">*Destination*</span><span class="sxs-lookup"><span data-stu-id="1f975-114">*Destination*</span></span> |<span data-ttu-id="1f975-115">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="1f975-115">Optional.</span></span> <span data-ttu-id="1f975-116">*ソース*のコピー先の場所を指定する URL を含む**文字列**値。</span><span class="sxs-lookup"><span data-stu-id="1f975-116">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>|
|<span data-ttu-id="1f975-117">*UserName*</span><span class="sxs-lookup"><span data-stu-id="1f975-117">*UserName*</span></span> |<span data-ttu-id="1f975-p103">省略可能です。*Destination* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1f975-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="1f975-120">*Password*</span><span class="sxs-lookup"><span data-stu-id="1f975-120">*Password*</span></span> |<span data-ttu-id="1f975-p104">省略可能です。*UserName* を確認するためのパスワードを含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1f975-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="1f975-123">*Options*</span><span class="sxs-lookup"><span data-stu-id="1f975-123">*Options*</span></span> |<span data-ttu-id="1f975-p105">省略可能です。[CopyRecordOptionsEnum](copyrecordoptionsenum.md) 値を指定します。既定値は、 **adCopyUnspecified** です。このメソッドの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1f975-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="1f975-127">*Async*</span><span class="sxs-lookup"><span data-stu-id="1f975-127">*Async*</span></span> |<span data-ttu-id="1f975-p106">省略可能です。ブール型 ( **Boolean** ) の値を指定します。値が **True** の場合、この動作は非同期で実行されます。</span><span class="sxs-lookup"><span data-stu-id="1f975-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="1f975-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="1f975-130">Return value</span></span>

<span data-ttu-id="1f975-p107">文字列型 (**String**) の値を返します。通常は、*Destination* の値が返されます。ただし、実際に返される値はプロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="1f975-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f975-133">備考</span><span class="sxs-lookup"><span data-stu-id="1f975-133">Remarks</span></span>

<span data-ttu-id="1f975-134">*送信元*と*送信先*の値いない必要があります同じです。それ以外の場合、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1f975-134">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="1f975-135">サーバー、パス、またはリソースの名前の少なくとも 1 つは異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f975-135">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="1f975-p109">*Source* の子 (サブディレクトリなど) はすべて、**adCopyNonRecursive** が指定されている場合を除き、そのとおりにコピーされます。サブディレクトリもコピーする場合は、*Destination* に *Source* のサブディレクトリを指定しないでください。指定した場合はコピー操作が完了しません。</span><span class="sxs-lookup"><span data-stu-id="1f975-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="1f975-138">**AdCopyOverWrite**を指定しない限り、*移動先*が (たとえば、ファイルまたはディレクトリ)、既存のエンティティを識別する場合、このメソッドが失敗します。</span><span class="sxs-lookup"><span data-stu-id="1f975-138">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f975-139">**AdCopyOverWrite**オプションを慎重に使用します。</span><span class="sxs-lookup"><span data-stu-id="1f975-139">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="1f975-140">などのディレクトリにファイルをコピーするときにこのオプションを指定するディレクトリは*削除*し、ファイルで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="1f975-140">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>


> [!NOTE]
> <span data-ttu-id="1f975-141">[!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1f975-141">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="1f975-142">詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f975-142">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


