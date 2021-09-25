---
title: TableDefs.Refresh メソッド (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5c31a3ec4d9b8ee2f44f7f9bad321a2483301263
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596898"
---
# <a name="tabledefsrefresh-method-dao"></a>TableDefs.Refresh メソッド (DAO)


**適用先**: Access 2013、Office 2013

指定されたコレクション内のオブジェクトを更新して、データベースの現在のスキーマを反映させます。

## <a name="syntax"></a>構文

*式* .更新

*式* TableDefs オブジェクトを **表す変数** 。

## <a name="remarks"></a>注釈

Microsoft Access データベース エンジンで **QueryDef**、 **Recordset**、または **TableDef** の各オブジェクトの **Fields** コレクションに含まれる **Field** オブジェクトに使用される場所を確認するには、各 **Field** オブジェクトの **OrdinalPosition** プロパティを使用します。 **Field** オブジェクトの **OrdinalPosition** プロパティを変更しても、 **Refresh** メソッドを使用しない限り、コレクションにおける **Field** オブジェクトの順序は変化しない場合があります。

**Refresh** メソッドは、他のユーザーがデータベースを変更する可能性のあるマルチユーザー環境で使用します。データベースに対する変更によって間接的に影響を受けるコレクションで、このメソッドを使用する必要があることもあります。たとえば、 **Users** コレクションを変更した場合は、 **Groups** コレクションを使用する前に **Groups** コレクションを更新する必要があることがあります。

コレクションのオブジェクトはそのコレクションが最初に参照されたときに設定され、それ以降に他のユーザーが行った変更は自動的には反映されません。他のユーザーがコレクションを変更した可能性がある場合は、コレクション内に特定のオブジェクトが存在する (または存在しない) ことを前提とするタスクをアプリケーションで実行する直前に、コレクションの Refresh メソッドを使用してください。これにより、コレクションを最新の状態にしておくことができます。一方、Refresh を使用すると、パフォーマンスが必要以上に低下する場合があります。

