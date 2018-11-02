---
title: メソッドを ActiveX データ オブジェクト (ADO) を読む
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6de4ea8a8dd64ff4c0562111f6e42ed089754f3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919459"
---
# <a name="read-method-ado"></a><span data-ttu-id="89d29-102">Read メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="89d29-102">Read method (ADO)</span></span>


<span data-ttu-id="89d29-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="89d29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89d29-104">バイナリ型の [Stream](stream-object-ado.md) オブジェクトから、指定されたバイト数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="89d29-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d29-105">構文</span><span class="sxs-lookup"><span data-stu-id="89d29-105">Syntax</span></span>

<span data-ttu-id="89d29-106">*バリアント* = *ストリーム*。読み取り (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="89d29-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="89d29-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89d29-107">Parameters</span></span>

  - <span data-ttu-id="89d29-108">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="89d29-108">*NumBytes*</span></span>

  - <span data-ttu-id="89d29-p101">省略可能です。ファイルから読み取るバイト数を指定する長整数型 ( **Long** ) の値、または [StreamReadEnum](streamreadenum.md) 値の **adReadAll** (既定値) を指定します。</span><span class="sxs-lookup"><span data-stu-id="89d29-p101">Optional. A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>

## <a name="return-value"></a><span data-ttu-id="89d29-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="89d29-111">Return value</span></span>

<span data-ttu-id="89d29-112">**Read** メソッドは、指定したバイト数またはストリーム全体を **Stream** オブジェクトから読み取り、結果のデータをバリアント型 ( **Variant** ) として返します。</span><span class="sxs-lookup"><span data-stu-id="89d29-112">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="89d29-113">解説</span><span class="sxs-lookup"><span data-stu-id="89d29-113">Remarks</span></span>

<span data-ttu-id="89d29-p102">*NumBytes* が **Stream** に残っているバイト数よりも大きい場合、残っているバイトのみが返されます。読み取ったデータに、*NumBytes* で指定した長さに合うようにスペースが補充されることはありません。読み取るデータが残っていない場合は、Null 値のバリアント型が返されます。**Read** を使用して逆方向の読み取りを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="89d29-p102">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned. The data read is not padded to match the length specified by *NumBytes*. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="89d29-p103"><EM>NumBytes</EM> は常にバイトを表します。テキストの <STRONG>Stream</STRONG> オブジェクト (<A href="type-property-ado-stream.md">Type</A> が <STRONG>adTypeText</STRONG>) の場合は、<A href="readtext-method-ado.md">ReadText</A> を使用してください。</span><span class="sxs-lookup"><span data-stu-id="89d29-p103"><EM>NumBytes</EM> always measures bytes. For text <STRONG>Stream</STRONG> objects (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>), use <A href="readtext-method-ado.md">ReadText</A>.</span></span></P>


