---
title: Append メソッド (ADOX Keys)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718904"
---
# <a name="append-method-adox-keys"></a>Append メソッド (ADOX Keys)

**適用されます**Access 2013、Office 2013。

新しい [Key](key-object-adox.md) オブジェクトを [Keys](keys-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*キー*。*キー*を追加する\[、*KeyType* \] \[、*列*\] \[、*RelatedTable* \] \[、*RelatedColumn*\]

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Key* |追加する **Key** オブジェクトを指定します。または、作成して追加するキーの名前を指定します。|
|*KeyType* |省略可能です。 キーの種類を示す長整数型 ( **Long** ) の値を指定します。 *Key*パラメーターは、**キー**オブジェクトの[Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox)プロパティに対応します。|
|*Column* |省略可能です。 インデックスが作成される列の名前を指定する文字列型 ( **String** ) の値を指定します。 *Columns*パラメーターは、 [Column](column-object-adox.md)オブジェクトの[Name](name-property-adox.md)プロパティの値に対応します。|
|*RelatedTable* |省略可能です。 リレーション テーブルの名前を示す文字列型 ( **String** ) の値を指定します。 *RelatedTable*パラメーターは、[テーブル](table-object-adox.md)オブジェクトの**Name**プロパティの値に対応します。|
|*RelatedColumn* |省略可能です。外部キーの関連する列の名前を示す文字列型 ( **String** ) の値を指定します。RelatedColumn パラメーターは、 **Column** オブジェクトの **Name** プロパティの値に対応します。|

## <a name="remarks"></a>解説

*Columns*パラメーターには、列の名前または列名の配列のいずれかを実行できます。

