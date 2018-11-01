---
title: LoadFromFile メソッド (ADO)
TOCTitle: LoadFromFile Method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 61244e989815d5c4ba1943e61aea7f6a6abf139d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872033"
---
# <a name="loadfromfile-method-ado"></a><span data-ttu-id="365ce-102">LoadFromFile メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="365ce-102">LoadFromFile Method (ADO)</span></span>


<span data-ttu-id="365ce-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="365ce-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="365ce-104">既存のファイルの内容を [Stream](stream-object-ado.md) に読み込みます。</span><span class="sxs-lookup"><span data-stu-id="365ce-104">Loads the contents of an existing file into a [Stream](stream-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="365ce-105">構文</span><span class="sxs-lookup"><span data-stu-id="365ce-105">Syntax</span></span>

<span data-ttu-id="365ce-106">*ストリーム*。LoadFromFile*ファイル名*</span><span class="sxs-lookup"><span data-stu-id="365ce-106">*Stream*.LoadFromFile *FileName*</span></span>

## <a name="parameter"></a><span data-ttu-id="365ce-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="365ce-107">Parameter</span></span>

  - <span data-ttu-id="365ce-108">*Filename*</span><span class="sxs-lookup"><span data-stu-id="365ce-108">*FileName*</span></span>

  - <span data-ttu-id="365ce-109">**Stream** に読み込むファイルの名前を含む文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="365ce-109">A **String** value that contains the name of a file to be loaded into the **Stream**.</span></span> <span data-ttu-id="365ce-110">*ファイル名*には、任意の有効なパスと UNC 形式の名前を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="365ce-110">*FileName* can contain any valid path and name in UNC format.</span></span> <span data-ttu-id="365ce-111">指定したファイルが存在しない場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="365ce-111">If the specified file does not exist, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="365ce-112">解説</span><span class="sxs-lookup"><span data-stu-id="365ce-112">Remarks</span></span>

<span data-ttu-id="365ce-p102">このメソッドを使用して、ローカル ファイルの内容を **Stream** オブジェクトに読み込むことができます。この方法で、ローカル ファイルの内容をサーバーにアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="365ce-p102">This method may be used to load the contents of a local file into a **Stream** object. This may be used to upload the contents of a local file to a server.</span></span>

<span data-ttu-id="365ce-p103">**Stream** オブジェクトは **LoadFromFile** を呼び出す前に開かれている必要があります。 **Stream** オブジェクトのバインディングはこのメソッドによって変更されず、その **Stream** を開いた URL または **Record** で指定されたオブジェクトにバインドされたままです。</span><span class="sxs-lookup"><span data-stu-id="365ce-p103">The **Stream** object must be already open before calling **LoadFromFile**. This method does not change the binding of the **Stream** object; it will still be bound to the object specified by the URL or **Record** with which the **Stream** was originally opened.</span></span>

<span data-ttu-id="365ce-p104">**LoadFromFile** では、 **Stream** オブジェクトの現在の内容を、ファイルから読み込んだデータで上書きします。 **Stream** の既存のすべてのバイトは、ファイルの内容で上書きされます。 [LoadFromFile](eos-property-ado.md) メソッドで作成された **EOS** の後に残っている既存のバイトは、すべて削除されます。</span><span class="sxs-lookup"><span data-stu-id="365ce-p104">**LoadFromFile** overwrites the current contents of the **Stream** object with data read from the file. Any existing bytes in the **Stream** are overwritten by the contents of the file. Any previously existing and remaining bytes following the [EOS](eos-property-ado.md) created by **LoadFromFile**, are truncated.</span></span>

<span data-ttu-id="365ce-120">**LoadFromFile** を呼び出した後、現在の位置は **Stream** の先頭に設定され、[Position](position-property-ado.md) プロパティが 0 になります。</span><span class="sxs-lookup"><span data-stu-id="365ce-120">After a call to **LoadFromFile**, the current position is set to the beginning of the **Stream** ([Position](position-property-ado.md) is 0).</span></span>

<span data-ttu-id="365ce-121">ストリームの先頭にエンコード用の 2 バイトを追加できるので、ストリームのサイズは読み込み元のファイルのサイズと完全には一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="365ce-121">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</span></span>

