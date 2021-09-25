---
title: Indexes.Refresh メソッド (DAO)
TOCTitle: Refresh Method
ms:assetid: ffe1bc79-5a56-2a70-c5ac-2f80b683adbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837325(v=office.15)
ms:contentKeyID: 48548973
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 841936104db21138a1d9d07129edb8bc59a9e01d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577270"
---
# <a name="indexesrefresh-method-dao"></a>Indexes.Refresh メソッド (DAO)


**適用先:** Access 2013、Office 2013

指定されたコレクション内のオブジェクトを更新して、データベースの現在のスキーマを反映させます。

## <a name="syntax"></a>構文

*式* .更新

*式* Indexes オブジェクトを **表す変数** 。

## <a name="remarks"></a>注釈

**Refresh** メソッドは、他のユーザーがデータベースを変更する可能性のあるマルチユーザー環境で使用します。データベースに対する変更によって間接的に影響を受けるコレクションで、このメソッドを使用する必要があることもあります。たとえば、 **Users** コレクションを変更した場合は、 **Groups** コレクションを使用する前に **Groups** コレクションを更新する必要があることがあります。

コレクションのオブジェクトはそのコレクションが最初に参照されたときに設定され、それ以降に他のユーザーが行った変更は自動的には反映されません。他のユーザーがコレクションを変更した可能性がある場合は、コレクション内に特定のオブジェクトが存在する (または存在しない) ことを前提とするタスクをアプリケーションで実行する直前に、コレクションの Refresh メソッドを使用してください。これにより、コレクションを最新の状態にしておくことができます。一方、Refresh を使用すると、パフォーマンスが必要以上に低下する場合があります。

