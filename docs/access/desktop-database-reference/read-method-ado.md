---
title: メソッドを ActiveX データ オブジェクト (ADO) を読む
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4fcc4c3039e1e55bb6bd33078542faa880d27ded
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477376"
---
# <a name="read-method-ado"></a><span data-ttu-id="c420d-102">Read メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="c420d-102">Read Method (ADO)</span></span>


<span data-ttu-id="c420d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c420d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c420d-104">バイナリ型の [Stream](stream-object-ado.md) オブジェクトから、指定されたバイト数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="c420d-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c420d-105">構文</span><span class="sxs-lookup"><span data-stu-id="c420d-105">Syntax</span></span>

<span data-ttu-id="c420d-106">*バリアント* = *ストリーム*。読み取り (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="c420d-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="c420d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c420d-107">Parameters</span></span>

  - <span data-ttu-id="c420d-108">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="c420d-108">*NumBytes*</span></span>

  - <span data-ttu-id="c420d-p101">省略可能です。ファイルから読み取るバイト数を指定する長整数型 ( **Long** ) の値、または [StreamReadEnum](streamreadenum.md) 値の **adReadAll** (既定値) を指定します。</span><span class="sxs-lookup"><span data-stu-id="c420d-p101">Optional. A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>

## <a name="return-value"></a><span data-ttu-id="c420d-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="c420d-111">Return Value</span></span>

<span data-ttu-id="c420d-112">**Read** メソッドは、指定したバイト数またはストリーム全体を **Stream** オブジェクトから読み取り、結果のデータをバリアント型 ( **Variant** ) として返します。</span><span class="sxs-lookup"><span data-stu-id="c420d-112">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c420d-113">解説</span><span class="sxs-lookup"><span data-stu-id="c420d-113">Remarks</span></span>

<span data-ttu-id="c420d-p102">*NumBytes* が **Stream** に残っているバイト数よりも大きい場合、残っているバイトのみが返されます。読み取ったデータに、*NumBytes* で指定した長さに合うようにスペースが補充されることはありません。読み取るデータが残っていない場合は、Null 値のバリアント型が返されます。**Read** を使用して逆方向の読み取りを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="c420d-p102">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned. The data read is not padded to match the length specified by *NumBytes*. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c420d-p103"><EM>NumBytes</EM> は常にバイトを表します。テキストの <STRONG>Stream</STRONG> オブジェクト (<A href="type-property-ado-stream.md">Type</A> が <STRONG>adTypeText</STRONG>) の場合は、<A href="readtext-method-ado.md">ReadText</A> を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c420d-p103"><EM>NumBytes</EM> always measures bytes. For text <STRONG>Stream</STRONG> objects (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>), use <A href="readtext-method-ado.md">ReadText</A>.</span></span></P>


