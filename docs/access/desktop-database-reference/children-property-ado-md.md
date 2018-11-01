---
title: Children プロパティ (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57049e0e68e4620664687cd261881af953de189f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875211"
---
# <a name="children-property-ado-md"></a>Children プロパティ (ADO MD)


**適用されます**Access 2013、Office 2013。

階層内で、現在の [Member](members-collection-ado-md.md) を親とする [Members](member-object-ado-md.md) コレクションを取得します。

## <a name="return-values"></a>戻り値

**Members** コレクションを取得します。値の取得のみが可能です。

## <a name="remarks"></a>解説

**Children** プロパティには、現在の **Member** を階層内で親とする **Members** コレクションが含まれます。リーフ レベルの **Member** オブジェクトには **Members** コレクションに子メンバーがありません。このプロパティは、 **Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトでのみサポートされています。 **Position** オブジェクトに属する [Member](position-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。

