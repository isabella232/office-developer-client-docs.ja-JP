---
title: Seek メソッド - ActiveX データ オブジェクト (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bdf15631bc1897158e5efab5712434a5ef61eb07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580877"
---
# <a name="seek-method-ado"></a>Seek メソッド (ADO)

**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) のインデックスを検索して、指定された値と一致する行をすばやく探し、その行をカレント行にします。

## <a name="syntax"></a>構文

*recordset*.Seek *KeyValues*, *SeekOption*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*KeyValues* |バリアント型 ( **Variant** ) の値の配列。インデックスは 1 つまたは複数の列から成るため、対応する各列と比較する値をこの配列に格納します。|
|*SeekOption* |インデックスの各列とそれに対応する *KeyValues* の比較に使用する比較の種類を指定する [SeekEnum](seekenum.md) 値。|

## <a name="remarks"></a>注釈

基になるプロバイダーが **Recordset** オブジェクトのインデックスをサポートしている場合、[Index](index-property-ado.md) プロパティと共に **Seek** メソッドを使用します。基になるプロバイダーが **Seek** をサポートしているかどうかを判別するには、[Supports](supports-method-ado.md)**(adSeek)** メソッドを使用します。プロバイダーがインデックスをサポートしているかどうかを判別するには、**Supports(adIndex)** メソッドを使用します。たとえば、[OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) は **Seek** および **Index** をサポートしています。

**Seek** メソッドで目的の行が見つからない場合、エラーは発生せず、行は **Recordset** の末尾に配置されます。このメソッドを実行する前に、 **Index** プロパティを必要なインデックスに設定してください。

このメソッドは、サーバー側のカーソルでのみサポートされます。 **Recordset** オブジェクトの [CursorLocation](cursorlocation-property-ado.md) プロパティの値が **adUseClient** になっている場合は、Seek はサポートされません。

このメソッドは、 **Recordset** オブジェクトが [CommandTypeEnum](commandtypeenum.md) の値を **adCmdTableDirect** にして開かれた場合にのみ使用できます。

