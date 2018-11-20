---
title: メソッド - を作成するには、ActiveX データ オブジェクト (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 227c7a3746d0c743c33f76362023d6d374269a81
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026282"
---
# <a name="write-method-ado"></a><span data-ttu-id="bb392-102">Write メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="bb392-102">Write method (ADO)</span></span>

<span data-ttu-id="bb392-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bb392-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb392-104">バイナリ データを [Stream](stream-object-ado.md) オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="bb392-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb392-105">構文</span><span class="sxs-lookup"><span data-stu-id="bb392-105">Syntax</span></span>

<span data-ttu-id="bb392-106">*ストリーム*。*バッファー*の書き込み</span><span class="sxs-lookup"><span data-stu-id="bb392-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="bb392-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="bb392-107">Parameters</span></span>

|<span data-ttu-id="bb392-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bb392-108">Parameter</span></span>|<span data-ttu-id="bb392-109">説明</span><span class="sxs-lookup"><span data-stu-id="bb392-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="bb392-110">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="bb392-110">*Buffer*</span></span> |<span data-ttu-id="bb392-111">書き込むバイト配列の入ったバリアント型 ( **Variant** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb392-111">A **Variant** that contains an array of bytes to be written.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bb392-112">解説</span><span class="sxs-lookup"><span data-stu-id="bb392-112">Remarks</span></span>

<span data-ttu-id="bb392-113">指定したバイトが、各バイト間にスペースを一切挿入することなく **Stream** オブジェクトに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="bb392-113">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="bb392-p101">カレント [Position](position-property-ado.md) は、書き込まれたデータの次のバイトに設定されます。 **Write** メソッドがストリーム内の残りのデータを切り捨てることはありません。後ろのバイトを切り捨てるには、 [SetEOS](seteos-method-ado.md) を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="bb392-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="bb392-117">現在の [EOS](eos-property-ado.md) 位置を越えて書き込みを行うと、新しいバイトがすべて格納できるように [Stream](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) の **Size** が大きくなり、 **EOS** が **Stream** 内の新しい末尾バイトへと移動します。</span><span class="sxs-lookup"><span data-stu-id="bb392-117">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="bb392-p102">**Write** メソッドは、バイナリ ストリーム ([Type](type-property-ado-stream.md) が **adTypeBinary**) で使用します。テキスト ストリーム (**Type** が **adTypeText**) の場合は、[WriteText](writetext-method-ado.md) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="bb392-p102">The **Write** method is used with binary streams ([Type](type-property-ado-stream.md) is **adTypeBinary**). For text streams (**Type** is **adTypeText**), use [WriteText](writetext-method-ado.md).</span></span>

