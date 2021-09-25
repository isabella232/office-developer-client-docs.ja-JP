---
title: Parent プロパティ (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 858978b45fd8ee687dd60619bbdb59c0eef01f68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617903"
---
# <a name="parent-property-ado-md"></a>Parent プロパティ (ADO MD)


**適用先**: Access 2013、Office 2013

階層内の現在のメンバーの親であるメンバーを示します。

## <a name="return-values"></a>戻り値

[Member](member-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

階層の最上位レベル (ルート) にあるメンバーには、親はありません。このプロパティは、[Level](level-object-ado-md.md) オブジェクトに属する **Member** オブジェクトでのみサポートされます。[Position](position-object-ado-md.md) オブジェクトに属する **Member** オブジェクトからこのプロパティが参照されると、エラーが発生します。

