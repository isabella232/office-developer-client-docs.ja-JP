---
title: ActiveX データ オブジェクト (ADO) メソッドをシークします。
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726303"
---
# <a name="seek-method-ado"></a><span data-ttu-id="f4262-102">Seek メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="f4262-102">Seek method (ADO)</span></span>

<span data-ttu-id="f4262-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f4262-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4262-104">[Recordset](recordset-object-ado.md) のインデックスを検索して、指定された値と一致する行をすばやく探し、その行をカレント行にします。</span><span class="sxs-lookup"><span data-stu-id="f4262-104">Searches the index of a [Recordset](recordset-object-ado.md) to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4262-105">構文</span><span class="sxs-lookup"><span data-stu-id="f4262-105">Syntax</span></span>

<span data-ttu-id="f4262-106">*レコード セット*です。*KeyValues*、 *SeekOption*を検索します。</span><span class="sxs-lookup"><span data-stu-id="f4262-106">*recordset*.Seek*KeyValues*, *SeekOption*</span></span>

## <a name="parameters"></a><span data-ttu-id="f4262-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f4262-107">Parameters</span></span>

|<span data-ttu-id="f4262-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f4262-108">Parameter</span></span>|<span data-ttu-id="f4262-109">説明</span><span class="sxs-lookup"><span data-stu-id="f4262-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f4262-110">*KeyValues*</span><span class="sxs-lookup"><span data-stu-id="f4262-110">*KeyValues*</span></span> |<span data-ttu-id="f4262-p101">バリアント型 ( **Variant** ) の値の配列。インデックスは 1 つまたは複数の列から成るため、対応する各列と比較する値をこの配列に格納します。</span><span class="sxs-lookup"><span data-stu-id="f4262-p101">An array of **Variant** values. An index consists of one or more columns and the array contains a value to compare against each corresponding column.</span></span>|
|<span data-ttu-id="f4262-113">*SeekOption*</span><span class="sxs-lookup"><span data-stu-id="f4262-113">*SeekOption*</span></span> |<span data-ttu-id="f4262-114">インデックスの各列とそれに対応する *KeyValues* の比較に使用する比較の種類を指定する [SeekEnum](seekenum.md) 値。</span><span class="sxs-lookup"><span data-stu-id="f4262-114">A [SeekEnum](seekenum.md) value that specifies the type of comparison to be made between the columns of the index and the corresponding *KeyValues*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f4262-115">解説</span><span class="sxs-lookup"><span data-stu-id="f4262-115">Remarks</span></span>

<span data-ttu-id="f4262-116">基になるプロバイダーが **Recordset** オブジェクトのインデックスをサポートしている場合は、 [Seek](index-property-ado.md) メソッドを **Index** プロパティと組み合わせて使用します。</span><span class="sxs-lookup"><span data-stu-id="f4262-116">Use the **Seek** method in conjunction with the [Index](index-property-ado.md) property if the underlying provider supports indexes on the **Recordset** object.</span></span> <span data-ttu-id="f4262-117">**シーク**を基になるプロバイダーがサポートしているかどうかを決定する[をサポートしています](supports-method-ado.md)**(adSeek)** メソッドと、プロバイダーがインデックスをサポートしているかどうかを決定する**Supports(adIndex)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f4262-117">Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes.</span></span> <span data-ttu-id="f4262-118">(たとえば、 [Microsoft Jet 用 OLE DB プロバイダー](microsoft-ole-db-provider-for-microsoft-jet.md)をサポートしている**検索**と**インデックス**。)</span><span class="sxs-lookup"><span data-stu-id="f4262-118">(For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="f4262-p103">**Seek** メソッドで目的の行が見つからない場合、エラーは発生せず、行は **Recordset** の末尾に配置されます。このメソッドを実行する前に、 **Index** プロパティを必要なインデックスに設定してください。</span><span class="sxs-lookup"><span data-stu-id="f4262-p103">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="f4262-p104">このメソッドは、サーバー側のカーソルでのみサポートされます。 **Recordset** オブジェクトの [CursorLocation](cursorlocation-property-ado.md) プロパティの値が **adUseClient** になっている場合は、Seek はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="f4262-p104">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="f4262-123">このメソッドは、 **Recordset** オブジェクトが [CommandTypeEnum](commandtypeenum.md) の値を **adCmdTableDirect** にして開かれた場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4262-123">This method can only be used when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

