---
title: Properties.Refresh メソッド (DAO)
TOCTitle: Refresh Method
ms:assetid: 71ba18fb-55a5-6a5f-3631-1c81c20f3369
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195805(v=office.15)
ms:contentKeyID: 48545593
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9d6b248bc4b8d9c1a9e01db0231bf58b16c36dd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719737"
---
# <a name="propertiesrefresh-method-dao"></a>Properties.Refresh メソッド (DAO)


**適用されます**Access 2013、Office 2013。

指定されたコレクション内のオブジェクトを更新して、データベースの現在のスキーマを反映させます。

## <a name="syntax"></a>構文

*式*です。更新

*式***プロパティ**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Refresh** メソッドは、マルチユーザー環境で、他のユーザーがデータベースを変更する可能性がある場合に使用します。このメソッドは、データベースに対する変更によって間接的に影響を受けるコレクションでも使用する必要がある場合があります。たとえば、 **Users** コレクションを変更した場合は、 **Groups** コレクションを使用する前に、その **Groups** コレクションを変更する必要がある場合があります。

コレクション内のオブジェクトは、そのコレクションが最初に参照されたときに格納され、それ以降に他のユーザーが加えた変更が自動的に反映されることはありません。他のユーザーがコレクションを変更した可能性が高い場合は、そのコレクション内の特定のオブジェクトが存在すること、または存在しないことを仮定したタスクをアプリケーションで実行する直前に、そのコレクションで Refresh メソッドを使用します。これにより、そのコレクションを最新の状態にしておくことができます。一方で、Refresh を使用すると、パフォーマンスが必要以上に低下する場合があります。

