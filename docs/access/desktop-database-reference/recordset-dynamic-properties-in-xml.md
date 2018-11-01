---
title: XML のレコードセットの動的プロパティ
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48714b9178e99cfd4ccf7738f3ad4a342572fdfa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884262"
---
# <a name="recordset-dynamic-properties-in-xml"></a>XML のレコードセットの動的プロパティ


**適用されます**Access 2013、Office 2013。

## <a name="recordset-dynamic-properties-in-xml"></a>XML のレコードセットの動的プロパティ

次に挙げる Client Cursor Engine からの、プロバイダー固有の **Recordset** プロパティは、現在 XML 形式で保存されています。

  - **Update Resync**

  - **Unique Table**

  - **Unique Schema**

  - **Unique Catalog**

  - **Resync Command**

  - **IRowsetChange**

  - **IRowsetUpdate**

  - **CommandTimeout**

  - **BatchSize**

  - **UpdateCriteria**

  - **Reshape Name**

  - **AutoRecalc**

これらのプロパティは、保存される **Recordset** の要素定義の属性として "Schema" セクションに保存されます。これらの属性は、行セット スキーマ名前空間で定義され、プレフィックスが "rs:" であることが必要です。

