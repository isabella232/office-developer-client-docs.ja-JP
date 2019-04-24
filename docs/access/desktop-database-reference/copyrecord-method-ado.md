---
title: copyrecord メソッド (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295528"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="ebe94-102">copyrecord メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="ebe94-102">CopyRecord method (ADO)</span></span>

<span data-ttu-id="ebe94-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebe94-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ebe94-104">**Record** で表されるエンティティを別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="ebe94-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe94-105">構文</span><span class="sxs-lookup"><span data-stu-id="ebe94-105">Syntax</span></span>

<span data-ttu-id="ebe94-106">*レコード*。copyrecord (*Source*、 *Destination*、 *UserName*、 *Password*、 *Options*、 *Async*)</span><span class="sxs-lookup"><span data-stu-id="ebe94-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="ebe94-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ebe94-107">Parameters</span></span>

|<span data-ttu-id="ebe94-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ebe94-108">Parameter</span></span>|<span data-ttu-id="ebe94-109">説明</span><span class="sxs-lookup"><span data-stu-id="ebe94-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ebe94-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="ebe94-110">*Source*</span></span> |<span data-ttu-id="ebe94-p101">省略可能です。コピー元のエンティティ (ファイル、ディレクトリなど) を指定する URL を含む文字列型 (**String**) の値を指定します。*Source* を省略した場合、または空の文字列を指定した場合、現在の [Record](record-object-ado.md) で表されているファイルまたはディレクトリがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ebe94-p101">Optional. A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory). If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>|
|<span data-ttu-id="ebe94-114">*Destination*</span><span class="sxs-lookup"><span data-stu-id="ebe94-114">*Destination*</span></span> |<span data-ttu-id="ebe94-115">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="ebe94-115">Optional.</span></span> <span data-ttu-id="ebe94-116">*Source* のコピー先の場所を指定する URL を含む文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebe94-116">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>|
|<span data-ttu-id="ebe94-117">*UserName*</span><span class="sxs-lookup"><span data-stu-id="ebe94-117">*UserName*</span></span> |<span data-ttu-id="ebe94-118">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="ebe94-118">Optional.</span></span> <span data-ttu-id="ebe94-119">*Destination* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebe94-119">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="ebe94-120">*Password*</span><span class="sxs-lookup"><span data-stu-id="ebe94-120">*Password*</span></span> |<span data-ttu-id="ebe94-121">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="ebe94-121">Optional.</span></span> <span data-ttu-id="ebe94-122">*UserName* を確認するためのパスワードを含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebe94-122">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="ebe94-123">*Options*</span><span class="sxs-lookup"><span data-stu-id="ebe94-123">*Options*</span></span> |<span data-ttu-id="ebe94-p105">省略可能です。[CopyRecordOptionsEnum](copyrecordoptionsenum.md) 値を指定します。既定値は、 **adCopyUnspecified** です。このメソッドの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebe94-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="ebe94-127">*Async*</span><span class="sxs-lookup"><span data-stu-id="ebe94-127">*Async*</span></span> |<span data-ttu-id="ebe94-p106">省略可能です。ブール型 ( **Boolean** ) の値を指定します。値が **True** の場合、この動作は非同期で実行されます。</span><span class="sxs-lookup"><span data-stu-id="ebe94-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="ebe94-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="ebe94-130">Return value</span></span>

<span data-ttu-id="ebe94-p107">文字列型 (**String**) の値を返します。通常は、*Destination* の値が返されます。ただし、実際に返される値はプロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="ebe94-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe94-133">注釈</span><span class="sxs-lookup"><span data-stu-id="ebe94-133">Remarks</span></span>

<span data-ttu-id="ebe94-p108">*Source* と *Destination* の値は異なっている必要があります。値が等しい場合、実行時エラーが発生します。サーバー名、パス名、リソース名のうち、少なくとも 1 つが異なっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ebe94-p108">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs. At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="ebe94-p109">*Source* の子 (サブディレクトリなど) はすべて、**adCopyNonRecursive** が指定されている場合を除き、そのとおりにコピーされます。サブディレクトリもコピーする場合は、*Destination* に *Source* のサブディレクトリを指定しないでください。指定した場合はコピー操作が完了しません。</span><span class="sxs-lookup"><span data-stu-id="ebe94-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="ebe94-138">*Destination* に既存のエンティティ (ファイル、ディレクトリなど) を指定する場合、**adCopyOverWrite** を指定していなければ、このメソッドは失敗します。</span><span class="sxs-lookup"><span data-stu-id="ebe94-138">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ebe94-139">Use the **adCopyOverWrite** option judiciously.</span><span class="sxs-lookup"><span data-stu-id="ebe94-139">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="ebe94-140">たとえば、ファイルをディレクトリにコピーするときにこのオプションを指定すると、ディレクトリが*削除*され、ファイルに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="ebe94-140">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>


> [!NOTE]
> <span data-ttu-id="ebe94-141">[!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ebe94-141">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="ebe94-142">詳細については、「[絶対 url と相対 url](absolute-and-relative-urls.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebe94-142">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


