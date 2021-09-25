---
title: Children プロパティ (ADO MD)
TOCTitle: Children property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ed91a9c3a35ea2b9229bd813c814572be5217237
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594476"
---
# <a name="children-property-ado-md"></a>Children プロパティ (ADO MD)


**適用先**: Access 2013、Office 2013

階層内で、現在の [Member](members-collection-ado-md.md) を親とする [Members](member-object-ado-md.md) コレクションを取得します。

## <a name="return-values"></a>戻り値

**Members** コレクションを取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

**Children** プロパティには、現在の **Member** を階層内で親とする **Members** コレクションが含まれます。リーフ レベルの **Member** オブジェクトには **Members** コレクションに子メンバーがありません。このプロパティは、[Level](level-object-ado-md.md) オブジェクトに属する **Member** オブジェクトでのみサポートされています。[Position](position-object-ado-md.md) オブジェクトに属する **Member** オブジェクトからこのプロパティが参照されると、エラーが発生します。

