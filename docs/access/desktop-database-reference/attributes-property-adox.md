---
title: Attributes プロパティ (ADOX)
TOCTitle: Attributes property (ADOX)
ms:assetid: d5227b10-4a9b-5a57-d5ab-bbdd3e89aa95
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250072(v=office.15)
ms:contentKeyID: 48547959
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 14a4c719723767be8cb8e7e2f8ed02b5d2d4a143
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698170"
---
# <a name="attributes-property-adox"></a>Attributes プロパティ (ADOX)


**適用されます**Access 2013、Office 2013。

列の属性を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

長整数型 ( **Long** ) の値を設定または返します。この値は [Column](column-object-adox.md) オブジェクトによって表されるテーブルの属性を指定し、 [ColumnAttributesEnum](columnattributesenum.md) 定数を組み合わせることができます。既定値は 0 (ゼロ) です。 **adColFixed** でも **adColNullable** でもありません。

