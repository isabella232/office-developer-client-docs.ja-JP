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
# <a name="seek-method-ado"></a>Seek メソッド (ADO)

**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) のインデックスを検索して、指定された値と一致する行をすばやく探し、その行をカレント行にします。

## <a name="syntax"></a>構文

*レコード セット*です。*KeyValues*、 *SeekOption*を検索します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*KeyValues* |バリアント型 ( **Variant** ) の値の配列。インデックスは 1 つまたは複数の列から成るため、対応する各列と比較する値をこの配列に格納します。|
|*SeekOption* |インデックスの各列とそれに対応する *KeyValues* の比較に使用する比較の種類を指定する [SeekEnum](seekenum.md) 値。|

## <a name="remarks"></a>解説

基になるプロバイダーが **Recordset** オブジェクトのインデックスをサポートしている場合は、 [Seek](index-property-ado.md) メソッドを **Index** プロパティと組み合わせて使用します。 **シーク**を基になるプロバイダーがサポートしているかどうかを決定する[をサポートしています](supports-method-ado.md)**(adSeek)** メソッドと、プロバイダーがインデックスをサポートしているかどうかを決定する**Supports(adIndex)** メソッドを使用します。 (たとえば、 [Microsoft Jet 用 OLE DB プロバイダー](microsoft-ole-db-provider-for-microsoft-jet.md)をサポートしている**検索**と**インデックス**。)

**Seek** メソッドで目的の行が見つからない場合、エラーは発生せず、行は **Recordset** の末尾に配置されます。このメソッドを実行する前に、 **Index** プロパティを必要なインデックスに設定してください。

このメソッドは、サーバー側のカーソルでのみサポートされます。 **Recordset** オブジェクトの [CursorLocation](cursorlocation-property-ado.md) プロパティの値が **adUseClient** になっている場合は、Seek はサポートされません。

このメソッドは、 **Recordset** オブジェクトが [CommandTypeEnum](commandtypeenum.md) の値を **adCmdTableDirect** にして開かれた場合にのみ使用できます。

