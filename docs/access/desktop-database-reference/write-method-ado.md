---
title: ActiveX データ オブジェクト (ADO) メソッドを作成します。
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5987b16c033b13be145e60317cdfdc821851be38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867413"
---
# <a name="write-method-ado"></a><span data-ttu-id="a5e23-102">Write メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="a5e23-102">Write Method (ADO)</span></span>


<span data-ttu-id="a5e23-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a5e23-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a5e23-104">バイナリ データを [Stream](stream-object-ado.md) オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="a5e23-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e23-105">構文</span><span class="sxs-lookup"><span data-stu-id="a5e23-105">Syntax</span></span>

<span data-ttu-id="a5e23-106">*ストリーム*。*バッファー*の書き込み</span><span class="sxs-lookup"><span data-stu-id="a5e23-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="a5e23-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a5e23-107">Parameters</span></span>

  - <span data-ttu-id="a5e23-108">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="a5e23-108">*Buffer*</span></span>

  - <span data-ttu-id="a5e23-109">書き込むバイト配列の入ったバリアント型 ( **Variant** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a5e23-109">A **Variant** that contains an array of bytes to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5e23-110">解説</span><span class="sxs-lookup"><span data-stu-id="a5e23-110">Remarks</span></span>

<span data-ttu-id="a5e23-111">指定したバイトが、各バイト間にスペースを一切挿入することなく **Stream** オブジェクトに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="a5e23-111">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="a5e23-p101">カレント [Position](position-property-ado.md) は、書き込まれたデータの次のバイトに設定されます。 **Write** メソッドがストリーム内の残りのデータを切り捨てることはありません。後ろのバイトを切り捨てるには、 [SetEOS](seteos-method-ado.md) を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="a5e23-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="a5e23-115">現在の [EOS](eos-property-ado.md) 位置を越えて書き込みを行うと、新しいバイトがすべて格納できるように [Stream](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) の **Size** が大きくなり、 **EOS** が **Stream** 内の新しい末尾バイトへと移動します。</span><span class="sxs-lookup"><span data-stu-id="a5e23-115">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a5e23-p102"><STRONG>Write</STRONG> メソッドは、バイナリ ストリーム (<A href="type-property-ado-stream.md">Type</A> が <STRONG>adTypeBinary</STRONG>) で使用します。テキスト ストリーム (<STRONG>Type</STRONG> が <STRONG>adTypeText</STRONG>) の場合は、<A href="writetext-method-ado.md">WriteText</A> を使用してください。</span><span class="sxs-lookup"><span data-stu-id="a5e23-p102">The <STRONG>Write</STRONG> method is used with binary streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeBinary</STRONG>). For text streams (<STRONG>Type</STRONG> is <STRONG>adTypeText</STRONG>), use <A href="writetext-method-ado.md">WriteText</A>.</span></span></P>


