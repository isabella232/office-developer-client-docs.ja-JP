---
title: Parent プロパティ (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0c0eef638cb76676cd2287a34c0e4b17bd89c4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287791"
---
# <a name="parent-property-ado-md"></a>Parent プロパティ (ADO MD)


**適用先:** Access 2013、Office 2013

階層内の現在のメンバーの親であるメンバーを示します。

## <a name="return-values"></a>戻り値

[Member](member-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。

## <a name="remarks"></a>注釈

階層の最上位レベル (ルート) にあるメンバーには、親はありません。このプロパティは、[Level](level-object-ado-md.md) オブジェクトに属する **Member** オブジェクトでのみサポートされます。[Position](position-object-ado-md.md) オブジェクトに属する **Member** オブジェクトからこのプロパティが参照されると、エラーが発生します。

