---
title: Append メソッド (ADOX Indexes)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ae56acce889c6931c30603c02869953b2141e210
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559011"
---
# <a name="append-method-adox-indexes"></a>Append メソッド (ADOX Indexes)


**適用先:** Access 2013、Office 2013



新しい [Index](index-object-adox.md) オブジェクトを [Indexes](indexes-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*インデックス .* Append *Index* \[ ,*Columns*\]

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Index* |追加する **Index** オブジェクトを指定します。または、新たに作成して追加するインデックスの名前を指定します。|
|*Columns* |省略可能です。インデックスが作成される列の名前を示すバリアント型 (**Variant**) の値を指定します。*Columns* パラメーターは、1 つ以上の [Column](column-object-adox.md) オブジェクトの [Name](name-property-adox.md) プロパティの値に対応します。|

## <a name="remarks"></a>注釈

*Columns* パラメーターは、列の名前または列の名前の配列のいずれかとなります。

プロバイダーがインデックスの作成をサポートしていない場合は、エラーが発生します。

