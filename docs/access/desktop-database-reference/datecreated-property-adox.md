---
title: datecreated プロパティプロパティ (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 59b19ab3be6633daf7295a63a33a31a34b64fbd7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294422"
---
# <a name="datecreated-property-adox"></a>datecreated プロパティプロパティ (ADOX)


**適用先:** Access 2013、Office 2013

オブジェクトが作成された日付を示します。

## <a name="return-values"></a>戻り値

作成された日付を示すバリアント型 ( **Variant** ) の値を返します。 プロバイダーが **DateCreated** をサポートしていない場合、値は Null 値になります。

## <a name="remarks"></a>注釈

新しく追加されたオブジェクトの **DateCreated** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、**DateCreated** プロパティの値を取得するには、[Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの [Refresh](refresh-method-ado.md) メソッドを呼び出す必要があります。

