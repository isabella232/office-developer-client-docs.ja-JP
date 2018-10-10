---
title: CopyRecord メソッド (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a54cf5f4d14b3e623a576dee99e1fabeb070e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477958"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="f944d-102">CopyRecord メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="f944d-102">CopyRecord Method (ADO)</span></span>


<span data-ttu-id="f944d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f944d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f944d-104">**Record** で表されるエンティティを別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="f944d-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="f944d-105">構文</span><span class="sxs-lookup"><span data-stu-id="f944d-105">Syntax</span></span>

<span data-ttu-id="f944d-106">*レコード*です。定義 (*ソース*、*変換先*、*ユーザー名*、*パスワード*、*オプション*、*非同期*)</span><span class="sxs-lookup"><span data-stu-id="f944d-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="f944d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f944d-107">Parameters</span></span>

  - <span data-ttu-id="f944d-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="f944d-108">*Source*</span></span>

  - <span data-ttu-id="f944d-109">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="f944d-109">Optional.</span></span> <span data-ttu-id="f944d-110">コピー元のエンティティ (ファイル、ディレクトリなど) を指定する URL を含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f944d-110">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="f944d-111">*ソース*を省略すると、空の文字列を指定する場合は、ファイルまたはディレクトリが現在の[レコード](record-object-ado.md)で表されますがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="f944d-111">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>

  - <span data-ttu-id="f944d-112">*Destination*</span><span class="sxs-lookup"><span data-stu-id="f944d-112">*Destination*</span></span>

  - <span data-ttu-id="f944d-113">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="f944d-113">Optional.</span></span> <span data-ttu-id="f944d-114">*ソース*のコピー先の場所を指定する URL を含む**文字列**値。</span><span class="sxs-lookup"><span data-stu-id="f944d-114">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>

  - <span data-ttu-id="f944d-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="f944d-115">*UserName*</span></span>

  - <span data-ttu-id="f944d-p103">省略可能です。*Destination* へのアクセス権が設定されている場合、アクセス権を持つユーザー ID を含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f944d-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="f944d-118">*Password*</span><span class="sxs-lookup"><span data-stu-id="f944d-118">*Password*</span></span>

  - <span data-ttu-id="f944d-p104">省略可能です。*UserName* を確認するためのパスワードを含む、文字列型 (**String**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f944d-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="f944d-121">*Options*</span><span class="sxs-lookup"><span data-stu-id="f944d-121">*Options*</span></span>

  - <span data-ttu-id="f944d-p105">省略可能です。[CopyRecordOptionsEnum](copyrecordoptionsenum.md) 値を指定します。既定値は、 **adCopyUnspecified** です。このメソッドの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f944d-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="f944d-125">*Async*</span><span class="sxs-lookup"><span data-stu-id="f944d-125">*Async*</span></span>

  - <span data-ttu-id="f944d-p106">省略可能です。ブール型 ( **Boolean** ) の値を指定します。値が **True** の場合、この動作は非同期で実行されます。</span><span class="sxs-lookup"><span data-stu-id="f944d-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>

## <a name="return-value"></a><span data-ttu-id="f944d-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="f944d-128">Return Value</span></span>

<span data-ttu-id="f944d-p107">文字列型 (**String**) の値を返します。通常は、*Destination* の値が返されます。ただし、実際に返される値はプロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f944d-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="f944d-131">備考</span><span class="sxs-lookup"><span data-stu-id="f944d-131">Remarks</span></span>

<span data-ttu-id="f944d-132">*送信元*と*送信先*の値いない必要があります同じです。それ以外の場合、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f944d-132">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="f944d-133">サーバー、パス、またはリソースの名前の少なくとも 1 つは異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f944d-133">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="f944d-p109">*Source* の子 (サブディレクトリなど) はすべて、**adCopyNonRecursive** が指定されている場合を除き、そのとおりにコピーされます。サブディレクトリもコピーする場合は、*Destination* に *Source* のサブディレクトリを指定しないでください。指定した場合はコピー操作が完了しません。</span><span class="sxs-lookup"><span data-stu-id="f944d-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="f944d-136">**AdCopyOverWrite**を指定しない限り、*移動先*が (たとえば、ファイルまたはディレクトリ)、既存のエンティティを識別する場合、このメソッドが失敗します。</span><span class="sxs-lookup"><span data-stu-id="f944d-136">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>


> [!IMPORTANT]
> <P><span data-ttu-id="f944d-137"><STRONG>AdCopyOverWrite</STRONG>オプションを慎重に使用します。</span><span class="sxs-lookup"><span data-stu-id="f944d-137">Use the <STRONG>adCopyOverWrite</STRONG> option judiciously.</span></span> <span data-ttu-id="f944d-138">などのディレクトリにファイルをコピーするときにこのオプションを指定するディレクトリは<EM>削除</EM>し、ファイルで置き換えます。</span><span class="sxs-lookup"><span data-stu-id="f944d-138">For example, specifying this option when copying a file to a directory will <EM>delete</EM> the directory and replace it with the file.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="f944d-p111">[!メモ] http 体系を使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f944d-p111">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>

