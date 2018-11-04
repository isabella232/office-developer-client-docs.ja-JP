---
title: メソッド - を作成するには、ActiveX データ オブジェクト (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 93336294380ffa207f47adbcad630be3fdd1a8b8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950217"
---
# <a name="write-method-ado"></a><span data-ttu-id="47ce4-102">Write メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="47ce4-102">Write method (ADO)</span></span>

<span data-ttu-id="47ce4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="47ce4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47ce4-104">バイナリ データを [Stream](stream-object-ado.md) オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="47ce4-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="47ce4-105">構文</span><span class="sxs-lookup"><span data-stu-id="47ce4-105">Syntax</span></span>

<span data-ttu-id="47ce4-106">*ストリーム*。*バッファー*の書き込み</span><span class="sxs-lookup"><span data-stu-id="47ce4-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="47ce4-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="47ce4-107">Parameters</span></span>

|<span data-ttu-id="47ce4-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="47ce4-108">Parameter</span></span>|<span data-ttu-id="47ce4-109">説明</span><span class="sxs-lookup"><span data-stu-id="47ce4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="47ce4-110">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="47ce4-110">*Buffer*</span></span> |<span data-ttu-id="47ce4-111">書き込むバイト配列の入ったバリアント型 ( **Variant** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="47ce4-111">A **Variant** that contains an array of bytes to be written.</span></span>|

## <a name="remarks"></a><span data-ttu-id="47ce4-112">解説</span><span class="sxs-lookup"><span data-stu-id="47ce4-112">Remarks</span></span>

<span data-ttu-id="47ce4-113">指定したバイトが、各バイト間にスペースを一切挿入することなく **Stream** オブジェクトに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="47ce4-113">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="47ce4-p101">カレント [Position](position-property-ado.md) は、書き込まれたデータの次のバイトに設定されます。 **Write** メソッドがストリーム内の残りのデータを切り捨てることはありません。後ろのバイトを切り捨てるには、 [SetEOS](seteos-method-ado.md) を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="47ce4-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="47ce4-117">現在の [EOS](eos-property-ado.md) 位置を越えて書き込みを行うと、新しいバイトがすべて格納できるように [Stream](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) の **Size** が大きくなり、 **EOS** が **Stream** 内の新しい末尾バイトへと移動します。</span><span class="sxs-lookup"><span data-stu-id="47ce4-117">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="47ce4-p102">**Write** メソッドは、バイナリ ストリーム ([Type](type-property-ado-stream.md) が **adTypeBinary**) で使用します。テキスト ストリーム (**Type** が **adTypeText**) の場合は、[WriteText](writetext-method-ado.md) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="47ce4-p102">The **Write** method is used with binary streams ([Type](type-property-ado-stream.md) is **adTypeBinary**). For text streams (**Type** is **adTypeText**), use [WriteText](writetext-method-ado.md).</span></span>

