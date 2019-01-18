---
title: XML でのレコードセットの動的プロパティ
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf2a15937f6bcfd9ededcfad0cf15c29faf6e577
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712835"
---
# <a name="recordset-dynamic-properties-in-xml"></a>XML でのレコードセットの動的プロパティ

**適用されます**Access 2013、Office 2013。

次に挙げる Client Cursor Engine からの、プロバイダー固有の **Recordset** プロパティは、現在 XML 形式で保存されています。

- **AutoRecalc**
- **BatchSize**
- **CommandTimeout**
- **IRowsetChange**
- **IRowsetUpdate**
- **Reshape Name**
- **Resync Command**
- **Unique Catalog**
- **Unique Schema**
- **Unique Table**
- **Update Resync**
- **UpdateCriteria**


これらのプロパティは、保存される **Recordset** の要素定義の属性として "Schema" セクションに保存されます。これらの属性は、行セット スキーマ名前空間で定義され、プレフィックスが "rs:" であることが必要です。

## <a name="see-also"></a>関連項目

- [ADO の動的プロパティ](ado-dynamic-properties.md)
