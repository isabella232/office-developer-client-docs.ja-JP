---
title: ReadText メソッド (ADO)
TOCTitle: ReadText Method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083dccd2c1d328e825a198008fd773bc3a592f6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605213"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="1fa7a-102">ReadText メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="1fa7a-102">ReadText Method (ADO)</span></span>


<span data-ttu-id="1fa7a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="1fa7a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1fa7a-104">文字列型の [Stream](stream-object-ado.md) オブジェクトから、指定された文字数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="1fa7a-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa7a-105">構文</span><span class="sxs-lookup"><span data-stu-id="1fa7a-105">Syntax</span></span>

<span data-ttu-id="1fa7a-106">*文字列* = *ストリーム*。ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="1fa7a-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="1fa7a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1fa7a-107">Parameters</span></span>

  - <span data-ttu-id="1fa7a-108">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="1fa7a-108">*NumChars*</span></span>

  - <span data-ttu-id="1fa7a-p101">省略可能です。ファイルから読み取る文字の数を指定する長整数型 ( **Long** ) の値、または [StreamReadEnum](streamreadenum.md) 値を指定します。既定値は **adReadAll** です。</span><span class="sxs-lookup"><span data-stu-id="1fa7a-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>

<span data-ttu-id="1fa7a-112"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="1fa7a-112"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="1fa7a-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="1fa7a-113">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="1fa7a-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="1fa7a-114">Return value</span></span>
>>>>>>> <span data-ttu-id="1fa7a-115">master</span><span class="sxs-lookup"><span data-stu-id="1fa7a-115">master</span></span>

<span data-ttu-id="1fa7a-116">**ReadText** メソッドは、指定した文字数、行全体、またはストリーム全体を **Stream** オブジェクトから読み取り、結果の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="1fa7a-116">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fa7a-117">解説</span><span class="sxs-lookup"><span data-stu-id="1fa7a-117">Remarks</span></span>

<span data-ttu-id="1fa7a-p102">*NumChar* がストリームに残っている文字の数よりも大きい場合、残っている文字のみが返されます。読み取った文字列に、*NumChar* で指定した長さに合うようにスペースが補充されることはありません。読み取る文字が残っていない場合は、値が Null のバリアント型が返されます。**ReadText** は、逆方向の読み取りに使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="1fa7a-p102">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned. The string read is not padded to match the length specified by *NumChar*. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1fa7a-p103"><STRONG>ReadText</STRONG> メソッドは、文字列型ストリーム (<A href="type-property-ado-stream.md">Type</A> が <STRONG>adTypeText</STRONG>) で使用します。バイナリ型のストリーム (<STRONG>Type</STRONG> が <STRONG>adTypeBinary</STRONG>) の場合は、<A href="read-method-ado.md">Read</A> を使用してください。</span><span class="sxs-lookup"><span data-stu-id="1fa7a-p103">The <STRONG>ReadText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="read-method-ado.md">Read</A>.</span></span></P>


