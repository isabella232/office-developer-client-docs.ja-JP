---
title: Property オブジェクト (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e26bc59221b4ff55c943b6a9a0c87ac5c0dd936b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301191"
---
# <a name="property-object-dao"></a>Property オブジェクト (DAO)

**適用先:** Access 2013、Office 2013

**Property** オブジェクトは、DAO オブジェクトの組み込みまたはユーザー定義の特性を表します。

## <a name="remarks"></a>注釈

**Connection** オブジェクトおよび **Error** オブジェクトを除くすべての DAO オブジェクトには、その DAO オブジェクトの組み込みプロパティに対応する **Property** オブジェクトを持つ **Properties** コレクションが含まれています。ユーザーは **Property** オブジェクトを定義して、DAO オブジェクトの **Properties** コレクションに追加することもできます。これらの **Property** オブジェクト (単にプロパティとも呼ばれる) により、オブジェクトのインスタンスに固有の属性が割り当てられます。

次のオブジェクトに対し、ユーザー定義のプロパティを作成することができます。

- **Database**、 **Index**、 **QueryDef**、および **TableDef** の各オブジェクト

- **QueryDef** オブジェクトおよび **TableDef** オブジェクトの **Fields** コレクションの **Field** オブジェクト

To add a user-defined property, use the **CreateProperty** method to create a **Property** object with a unique **Name** property setting. Set the **Type** and **Value** properties of the new **Property** object, and then append it to the **Properties** collection of the appropriate object. The object to which you are adding the user-defined property must already be appended to a collection. Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.

**Properties** コレクションからユーザー定義のプロパティを削除することはできますが、組み込みプロパティは削除できません。

> [!NOTE]
> [!メモ] ユーザー定義の **Property** オブジェクトは、1 つのオブジェクトの特定のインスタンスにのみ関連付けられます。プロパティは、選択した種類のオブジェクトのすべてのインスタンスに定義されるわけではありません。

オブジェクトの **Properties** コレクションを使用して、オブジェクトの組み込みおよびユーザー定義のプロパティを列挙することができます。 この操作を行うために、既存のプロパティの種類や属性 (**Name** プロパティや **Type** プロパティ) をあらかじめ知っている必要はありません。 ただし、値の取得のみ可能なプロパティ ( **Workspace** オブジェクトの **Password** プロパティなど) の読み取り、または不適切なコンテキストでのプロパティの読み取り/書き込み ( **TableDef** オブジェクトの **Fields** コレクションの **Field** オブジェクトの **Value** プロパティの設定など) を実行しようとすると、エラーが発生します。

**Property** オブジェクトには、次の 4 つの組み込みプロパティもあります。

- **Name** プロパティは、プロパティを一意に識別する文字列型 ( **String**) の値を格納します。

- **Type** プロパティは、プロパティのデータ型を指定する整数型 ( **Integer**) の値を格納します。

- **Value** プロパティは、プロパティの設定値を表すバリアント型 ( **Variant**) の値を格納します。

- **Inherited** プロパティは、そのプロパティが別のオブジェクトから継承されるかどうかを示すブール型 ( **Boolean**) の値を格納します。たとえば、 **Recordset** オブジェクトの **Fields** コレクションの **Field** オブジェクトは、基になる **TableDef** オブジェクトまたは **QueryDef** オブジェクトのプロパティを継承できます。

コレクション内の組み込みの **Property** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。

- * object ***.プロパティ**(0)

- *オブジェクト ***。プロパティ**("* name *")

- *オブジェクト ***。** プロパティ\!* 名 *\]

組み込みプロパティの場合、次の構文を使用することもできます。

- *オブジェクト*。*名前*

> [!NOTE]
> ユーザー定義のプロパティの場合は、完全なオブジェクト * を使用する必要があり***ます。プロパティ**("* name *") の構文。

同じ構文を使って、 **Property** オブジェクトの **Value** プロパティを参照することもできます。 **Property** オブジェクト自身と **Property** オブジェクトの **Value** プロパティのいずれを参照するかは、参照のコンテキストで決まります。

