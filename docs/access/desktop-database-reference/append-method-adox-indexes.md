---
title: Append メソッド (ADOX Indexes)
TOCTitle: Append Method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f91535075c2782861dc409a6c527f159cd5458a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477020"
---
# <a name="append-method-adox-indexes"></a>Append メソッド (ADOX Indexes)


**適用されます**Access 2013 |。Office 2013



新しい [Index](index-object-adox.md) オブジェクトを [Indexes](indexes-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*インデックス*です。*インデックス*を追加する\[、*列*\]

## <a name="parameters"></a>パラメーター

  - *Index*

  - 追加する **Index** オブジェクトを指定します。または、新たに作成して追加するインデックスの名前を指定します。

  - *Columns*

  - 省略可能です。 インデックスが作成される列の名前を示すバリアント型 ( **Variant** ) の値を指定します。 *Columns*パラメーターは、[列](column-object-adox.md)オブジェクトまたはオブジェクトの[Name](name-property-adox.md)プロパティの値に対応します。

## <a name="remarks"></a>備考

*Columns*パラメーターには、列の名前または列名の配列のいずれかを実行できます。

プロバイダーがインデックスの作成をサポートしていない場合は、エラーが発生します。

