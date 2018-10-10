---
title: Attributes プロパティ (ADOX)
TOCTitle: Attributes Property (ADOX)
ms:assetid: d5227b10-4a9b-5a57-d5ab-bbdd3e89aa95
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250072(v=office.15)
ms:contentKeyID: 48547959
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7eefb2a3582f177e2a5de5597d2150b0030a882
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476252"
---
# <a name="attributes-property-adox"></a>Attributes プロパティ (ADOX)


**適用されます**Access 2013 |。Office 2013

列の属性を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

長整数型 ( **Long** ) の値を設定または返します。この値は [Column](column-object-adox.md) オブジェクトによって表されるテーブルの属性を指定し、 [ColumnAttributesEnum](columnattributesenum.md) 定数を組み合わせることができます。既定値は 0 (ゼロ) です。 **adColFixed** でも **adColNullable** でもありません。

