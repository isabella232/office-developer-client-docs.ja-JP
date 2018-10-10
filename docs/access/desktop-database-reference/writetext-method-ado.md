---
title: WriteText メソッド (ADO)
TOCTitle: WriteText Method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67dcf218814f938c4583ba9587085cff73066dc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479610"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="8e67b-102">WriteText メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="8e67b-102">WriteText Method (ADO)</span></span>


<span data-ttu-id="8e67b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e67b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8e67b-104">指定されたテキスト文字列を [Stream](stream-object-ado.md) オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="8e67b-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e67b-105">構文</span><span class="sxs-lookup"><span data-stu-id="8e67b-105">Syntax</span></span>

<span data-ttu-id="8e67b-106">*ストリーム*。WriteText*データ*、*オプション*</span><span class="sxs-lookup"><span data-stu-id="8e67b-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="8e67b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8e67b-107">Parameters</span></span>

  - <span data-ttu-id="8e67b-108">*Data*</span><span class="sxs-lookup"><span data-stu-id="8e67b-108">*Data*</span></span>

  - <span data-ttu-id="8e67b-109">書き込むテキストが格納された文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e67b-109">A **String** value that contains the text in characters to be written.</span></span>

  - <span data-ttu-id="8e67b-110">*Options*</span><span class="sxs-lookup"><span data-stu-id="8e67b-110">*Options*</span></span>

  - <span data-ttu-id="8e67b-p101">省略可能です。指定された文字列の末尾に行区切り文字を書き込むかどうかを指定する [StreamWriteEnum](streamwriteenum.md) 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e67b-p101">Optional. A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e67b-113">解説</span><span class="sxs-lookup"><span data-stu-id="8e67b-113">Remarks</span></span>

<span data-ttu-id="8e67b-114">指定した文字列が、各文字列間にスペースや文字を挿入することなく **Stream** オブジェクトに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="8e67b-114">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="8e67b-p102">カレント [Position](position-property-ado.md) は、書き込まれたデータの次の文字に設定されます。 **WriteText** メソッドがストリーム内の残りのデータを切り捨てることはありません。後ろの文字を切り捨てるには、 [SetEOS](seteos-method-ado.md) を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="8e67b-p102">The current [Position](position-property-ado.md) is set to the character following the written data. The **WriteText** method does not truncate the rest of the data in a stream. If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="8e67b-118">現在の [EOS](eos-property-ado.md) 位置を越えて書き込みを行うと、新しい文字がすべて格納できるように [Stream](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) の **Size** が大きくなり、 **EOS** が **Stream** 内の新しい末尾バイトへと移動します。</span><span class="sxs-lookup"><span data-stu-id="8e67b-118">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8e67b-p103"><STRONG>WriteText</STRONG> メソッドは、テキスト ストリーム (<A href="type-property-ado-stream.md">Type</A> が <STRONG>adTypeText</STRONG>) で使用します。バイナリ ストリーム (<STRONG>Type</STRONG> が <STRONG>adTypeBinary</STRONG>) の場合は、<A href="write-method-ado.md">Write</A> を使用してください。</span><span class="sxs-lookup"><span data-stu-id="8e67b-p103">The <STRONG>WriteText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>). For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="write-method-ado.md">Write</A>.</span></span></P>


