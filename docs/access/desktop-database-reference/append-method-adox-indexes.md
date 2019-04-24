---
title: Append メソッド (ADOX Indexes)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297096"
---
# <a name="append-method-adox-indexes"></a>Append メソッド (ADOX Indexes)


**適用先:** Access 2013、Office 2013



新しい [Index](index-object-adox.md) オブジェクトを [Indexes](indexes-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*インデックス*。追加*インデックス* \[、*列*\]

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Index* |追加する **Index** オブジェクトを指定します。または、新たに作成して追加するインデックスの名前を指定します。|
|*Columns* |省略可能です。インデックスが作成される列の名前を示すバリアント型 (**Variant**) の値を指定します。*Columns* パラメーターは、1 つ以上の [Column](column-object-adox.md) オブジェクトの [Name](name-property-adox.md) プロパティの値に対応します。|

## <a name="remarks"></a>注釈

*Columns* パラメーターは、列の名前または列の名前の配列のいずれかとなります。

プロバイダーがインデックスの作成をサポートしていない場合は、エラーが発生します。

