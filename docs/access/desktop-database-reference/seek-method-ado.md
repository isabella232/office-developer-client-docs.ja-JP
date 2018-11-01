---
title: ActiveX データ オブジェクト (ADO) メソッドをシークします。
TOCTitle: Seek Method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb6a5a72474b8d19efe1dd155950fa9e3ecd8714
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889519"
---
# <a name="seek-method-ado"></a>Seek メソッド (ADO)


**適用されます**Access 2013、Office 2013。



[Recordset](recordset-object-ado.md) のインデックスを検索して、指定された値と一致する行をすばやく探し、その行をカレント行にします。

## <a name="syntax"></a>構文

*レコード セット*です。*KeyValues*、 *SeekOption*を検索します。

## <a name="parameters"></a>パラメーター

  - *KeyValues*

  - バリアント型 ( **Variant** ) の値の配列。インデックスは 1 つまたは複数の列から成るため、対応する各列と比較する値をこの配列に格納します。

  - *SeekOption*

  - インデックスの各列とそれに対応する *KeyValues* の比較に使用する比較の種類を指定する [SeekEnum](seekenum.md) 値。

## <a name="remarks"></a>解説

基になるプロバイダーが **Recordset** オブジェクトのインデックスをサポートしている場合は、 [Seek](index-property-ado.md) メソッドを **Index** プロパティと組み合わせて使用します。 **シーク**を基になるプロバイダーがサポートしているかどうかを決定する[をサポートしています](supports-method-ado.md)**(adSeek)** メソッドと、プロバイダーがインデックスをサポートしているかどうかを決定する**Supports(adIndex)** メソッドを使用します。 (たとえば、 [Microsoft Jet 用 OLE DB プロバイダー](microsoft-ole-db-provider-for-microsoft-jet.md)をサポートしている**検索**と**インデックス**。)

**Seek** メソッドで目的の行が見つからない場合、エラーは発生せず、行は **Recordset** の末尾に配置されます。このメソッドを実行する前に、 **Index** プロパティを必要なインデックスに設定してください。

このメソッドは、サーバー側のカーソルでのみサポートされます。 **Recordset** オブジェクトの [CursorLocation](cursorlocation-property-ado.md) プロパティの値が **adUseClient** になっている場合は、Seek はサポートされません。

このメソッドは、 **Recordset** オブジェクトが [CommandTypeEnum](commandtypeenum.md) の値を **adCmdTableDirect** にして開かれた場合にのみ使用できます。

