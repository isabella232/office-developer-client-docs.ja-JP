---
title: Parent プロパティ (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c183c997a3c0b49c74e08f7ef29fbe8c274516
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603337"
---
# <a name="parent-property-ado-md"></a>Parent プロパティ (ADO MD)


**適用されます**Access 2013 |。Office 2013

階層内の現在のメンバーの親であるメンバーを示します。

<<<<<<< ヘッド
## <a name="return-values"></a>戻り値
=======
## <a name="return-values"></a>戻り値
>>>>>>> master

[Member](member-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。

## <a name="remarks"></a>解説

階層の最上位レベル (ルート) にあるメンバーには、親はありません。このプロパティは、**Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトでのみサポートされます。 **Position** オブジェクトに属する [Member](position-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。

