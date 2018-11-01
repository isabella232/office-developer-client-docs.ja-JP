---
title: CopyTo メソッド (ADO)
TOCTitle: CopyTo Method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a5e5b793940c82e6656ec836c5a8d392800940d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870143"
---
# <a name="copyto-method-ado"></a><span data-ttu-id="64152-102">CopyTo メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="64152-102">CopyTo Method (ADO)</span></span>


<span data-ttu-id="64152-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="64152-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="64152-104">[Stream](type-property-ado-stream.md) オブジェクトから、指定した文字数またはバイト数 ( [Type](stream-object-ado.md) によって決まる) のデータを別の **Stream** オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="64152-104">Copies the specified number of characters or bytes (depending on [Type](type-property-ado-stream.md)) in the [Stream](stream-object-ado.md) to another **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="64152-105">構文</span><span class="sxs-lookup"><span data-stu-id="64152-105">Syntax</span></span>

<span data-ttu-id="64152-106">*ストリーム*。CopyTo *DestStream*、 *NumChars*</span><span class="sxs-lookup"><span data-stu-id="64152-106">*Stream*.CopyTo *DestStream*, *NumChars*</span></span>

## <a name="parameters"></a><span data-ttu-id="64152-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="64152-107">Parameters</span></span>

  - <span data-ttu-id="64152-108">*DestStream*</span><span class="sxs-lookup"><span data-stu-id="64152-108">*DestStream*</span></span>

  - <span data-ttu-id="64152-p101">開いている **Stream** オブジェクトへの参照を含むオブジェクト変数の値を指定します。*DestStream* で指定した **Stream** に現在の **Stream** がコピーされます。コピー先の **Stream** は既に開かれている必要があります。開かれていない場合は、実行時エラーが発生します。

</span><span class="sxs-lookup"><span data-stu-id="64152-p101">An object variable value that contains a reference to an open **Stream** object. The current **Stream** is copied to the destination **Stream** specified by *DestStream*. The destination **Stream** must already be open. If not, a run-time error occurs.</span></span>   

    > [!NOTE]
    > <span data-ttu-id="64152-113">*DestStream*パラメーターはありません、 **Stream**オブジェクトのプロキシ クライアントをリモート化不可能な**ストリーム**オブジェクトのプライベート インターフェイスへのアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="64152-113">The *DestStream* parameter may not be a proxy of the **Stream** object because this requires access to a private interface on the **Stream** object that cannot be remoted to the client.</span></span>

  - <span data-ttu-id="64152-114">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="64152-114">*NumChars*</span></span>

  - <span data-ttu-id="64152-115">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="64152-115">Optional.</span></span> <span data-ttu-id="64152-116">コピー元 **Stream** の現在の位置からコピー先の **Stream** にコピーするバイト数または文字数を指定する整数型 ( **Integer** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="64152-116">An **Integer** value that specifies the number of bytes or characters to be copied from the current position in the source **Stream** to the destination **Stream**.</span></span> <span data-ttu-id="64152-117">既定値は、-1 で、すべての文字またはバイトを[eos](eos-property-ado.md)の現在の位置からコピーされるように指定します。</span><span class="sxs-lookup"><span data-stu-id="64152-117">The default value is –1, which specifies that all characters or bytes are copied from the current position to [EOS](eos-property-ado.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="64152-118">解説</span><span class="sxs-lookup"><span data-stu-id="64152-118">Remarks</span></span>

<span data-ttu-id="64152-119">このメソッドは、[Position](position-property-ado.md) プロパティで指定された現在の位置から指定数の文字またはバイトをコピーします。</span><span class="sxs-lookup"><span data-stu-id="64152-119">This method copies the specified number of characters or bytes, starting from the current position specified by the [Position](position-property-ado.md) property.</span></span> <span data-ttu-id="64152-120">指定した数が、現在の位置から **EOS** までのバイト数を超える場合は、現在の位置から **EOS** までの文字またはバイトのみがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="64152-120">If the specified number is more than the available number of bytes until **EOS**, then only characters or bytes from the current position to **EOS** are copied.</span></span> <span data-ttu-id="64152-121">*NumChars*の値は-1、または省略すると、すべての文字または現在の位置から始まるバイトがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="64152-121">If the value of *NumChars* is –1, or omitted, all characters or bytes starting from the current position are copied.</span></span>

<span data-ttu-id="64152-p104">コピー先のストリームに既存の文字またはバイトが存在する場合、コピーの終了ポイント以降の内容はすべてそのまま残り、削除されません。 **Position** は、コピーされた最後のバイトの次のバイトになります。これらのバイトを削除する場合は、 [SetEOS](seteos-method-ado.md) を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="64152-p104">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated. **Position** becomes the byte immediately following the last byte copied. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="64152-p105">**CopyTo** メソッドは、コピー先の **Stream** とコピー元の **Stream** の種類が同じ場合 (**Type** プロパティの設定値がいずれも **adTypeText** であるか、またはいずれも **adTypeBinary** である場合) のコピーに使用します。**Stream** オブジェクトが文字列型の場合、コピー先の **Stream** の [Charset](charset-property-ado.md) プロパティの設定値を変更すると、文字セットを別の文字セットに変換することができます。また、文字列型の **Stream** オブジェクトをバイナリ型の **Stream** オブジェクトにコピーすることはできますが、バイナリ型の **Stream** オブジェクトを文字列型の **Stream** オブジェクトにコピーすることはできません。</span><span class="sxs-lookup"><span data-stu-id="64152-p105">**CopyTo** should be used to copy data to a destination **Stream** of the same type as the source **Stream** (their **Type** property settings are both **adTypeText** or both **adTypeBinary**). For text **Stream** objects, you can change the [Charset](charset-property-ado.md) property setting of the destination **Stream** to translate from one character set to another. Also, text **Stream** objects can be successfully copied into binary **Stream** objects, but binary **Stream** objects cannot be copied into text **Stream** objects.</span></span>

