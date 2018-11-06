---
title: LoadFromFile メソッド (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7b8492da87d0443d7992a1b9443501885ade3a0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998582"
---
# <a name="loadfromfile-method-ado"></a><span data-ttu-id="da630-102">LoadFromFile メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="da630-102">LoadFromFile method (ADO)</span></span>

<span data-ttu-id="da630-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="da630-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da630-104">既存のファイルの内容を [Stream](stream-object-ado.md) に読み込みます。</span><span class="sxs-lookup"><span data-stu-id="da630-104">Loads the contents of an existing file into a [Stream](stream-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="da630-105">構文</span><span class="sxs-lookup"><span data-stu-id="da630-105">Syntax</span></span>

<span data-ttu-id="da630-106">*ストリーム*。LoadFromFile*ファイル名*</span><span class="sxs-lookup"><span data-stu-id="da630-106">*Stream*.LoadFromFile *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="da630-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="da630-107">Parameters</span></span>

|<span data-ttu-id="da630-108">名前</span><span class="sxs-lookup"><span data-stu-id="da630-108">Name</span></span> |<span data-ttu-id="da630-109">説明</span><span class="sxs-lookup"><span data-stu-id="da630-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="da630-110">*Filename*</span><span class="sxs-lookup"><span data-stu-id="da630-110">*FileName*</span></span> |<span data-ttu-id="da630-111">**Stream** に読み込むファイルの名前を含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="da630-111">A **String** value that contains the name of a file to be loaded into the **Stream**.</span></span> <span data-ttu-id="da630-112">*ファイル名*には、任意の有効なパスと UNC 形式の名前を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="da630-112">*FileName* can contain any valid path and name in UNC format.</span></span> <span data-ttu-id="da630-113">指定したファイルが存在しない場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="da630-113">If the specified file does not exist, a run-time error occurs.</span></span>|

## <a name="remarks"></a><span data-ttu-id="da630-114">解説</span><span class="sxs-lookup"><span data-stu-id="da630-114">Remarks</span></span>

<span data-ttu-id="da630-p102">このメソッドを使用して、ローカル ファイルの内容を **Stream** オブジェクトに読み込むことができます。この方法で、ローカル ファイルの内容をサーバーにアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="da630-p102">This method may be used to load the contents of a local file into a **Stream** object. This may be used to upload the contents of a local file to a server.</span></span>

<span data-ttu-id="da630-p103">**Stream** オブジェクトは **LoadFromFile** を呼び出す前に開かれている必要があります。 **Stream** オブジェクトのバインディングはこのメソッドによって変更されず、その **Stream** を開いた URL または **Record** で指定されたオブジェクトにバインドされたままです。</span><span class="sxs-lookup"><span data-stu-id="da630-p103">The **Stream** object must be already open before calling **LoadFromFile**. This method does not change the binding of the **Stream** object; it will still be bound to the object specified by the URL or **Record** with which the **Stream** was originally opened.</span></span>

<span data-ttu-id="da630-p104">**LoadFromFile** では、 **Stream** オブジェクトの現在の内容を、ファイルから読み込んだデータで上書きします。 **Stream** の既存のすべてのバイトは、ファイルの内容で上書きされます。 [LoadFromFile](eos-property-ado.md) メソッドで作成された **EOS** の後に残っている既存のバイトは、すべて削除されます。</span><span class="sxs-lookup"><span data-stu-id="da630-p104">**LoadFromFile** overwrites the current contents of the **Stream** object with data read from the file. Any existing bytes in the **Stream** are overwritten by the contents of the file. Any previously existing and remaining bytes following the [EOS](eos-property-ado.md) created by **LoadFromFile**, are truncated.</span></span>

<span data-ttu-id="da630-122">**LoadFromFile** を呼び出した後、現在の位置は **Stream** の先頭に設定され、[Position](position-property-ado.md) プロパティが 0 になります。</span><span class="sxs-lookup"><span data-stu-id="da630-122">After a call to **LoadFromFile**, the current position is set to the beginning of the **Stream** ([Position](position-property-ado.md) is 0).</span></span>

<span data-ttu-id="da630-123">ストリームの先頭にエンコード用の 2 バイトを追加できるので、ストリームのサイズは読み込み元のファイルのサイズと完全には一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="da630-123">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</span></span>

