---
title: DateCreated プロパティ (ADOX)
TOCTitle: DateCreated Property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fea3e83f9a171a95eb844d9ba721039969804acf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876471"
---
# <a name="datecreated-property-adox"></a>DateCreated プロパティ (ADOX)


**適用されます**Access 2013、Office 2013。

オブジェクトが作成された日付を示します。

## <a name="return-values"></a>戻り値

作成された日付を示すバリアント型 ( **Variant** ) の値を返します。プロバイダーが **DateCreated** をサポートしていない場合、値は Null 値になります。

## <a name="remarks"></a>解説

新しく追加されたオブジェクトの **DateCreated** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、 [DateCreated](refresh-method-ado.md) プロパティの値を取得するには、 [Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの **Refresh** メソッドを呼び出す必要があります。

