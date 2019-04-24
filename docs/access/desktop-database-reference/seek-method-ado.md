---
title: Seek メソッド-ActiveX データオブジェクト (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308793"
---
# <a name="seek-method-ado"></a>Seek メソッド (ADO)

**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) のインデックスを検索して、指定された値と一致する行をすばやく探し、その行をカレント行にします。

## <a name="syntax"></a>構文

*recordset*。Seek*keyvalues*, *seekoption*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*KeyValues* |バリアント型 ( **Variant** ) の値の配列。インデックスは 1 つまたは複数の列から成るため、対応する各列と比較する値をこの配列に格納します。|
|*seekoption* |インデックスの各列とそれに対応する *KeyValues* の比較に使用する比較の種類を指定する [SeekEnum](seekenum.md) 値。|

## <a name="remarks"></a>注釈

基になるプロバイダーが **Recordset** オブジェクトのインデックスをサポートしている場合、[Index](index-property-ado.md) プロパティと共に **Seek** メソッドを使用します。基になるプロバイダーが **Seek** をサポートしているかどうかを判別するには、[Supports](supports-method-ado.md)**(adSeek)** メソッドを使用します。プロバイダーがインデックスをサポートしているかどうかを判別するには、**Supports(adIndex)** メソッドを使用します。たとえば、[OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) は **Seek** および **Index** をサポートしています。

**Seek** メソッドで目的の行が見つからない場合、エラーは発生せず、行は **Recordset** の末尾に配置されます。このメソッドを実行する前に、 **Index** プロパティを必要なインデックスに設定してください。

このメソッドは、サーバー側のカーソルでのみサポートされます。 **Recordset** オブジェクトの [CursorLocation](cursorlocation-property-ado.md) プロパティの値が **adUseClient** になっている場合は、Seek はサポートされません。

このメソッドは、 **Recordset** オブジェクトが [CommandTypeEnum](commandtypeenum.md) の値を **adCmdTableDirect** にして開かれた場合にのみ使用できます。

