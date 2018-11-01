---
title: State プロパティ (ADO MD)
TOCTitle: State Property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bc1efc33aa263275ba50526ff682b64a229293f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885466"
---
# <a name="state-property-ado-md"></a>State プロパティ (ADO MD)


**適用されます**Access 2013、Office 2013。

セルセットの現在の状態を示します。

## <a name="return-values"></a>戻り値

**Cellset** オブジェクトの現在の状態を示す長整数型 ( [Long](cellset-object-ado-md.md) ) の値を取得します。値の取得のみが可能です。有効な値は、 **adStateClosed** (0) および **adStateOpen** (1) です。

## <a name="remarks"></a>解説

[ObjectStateEnum](objectstateenum.md) 定数の名前を使用するには、プロジェクトで ADO タイプ ライブラリが参照されている必要があります。詳細については、「 [ADO と ADO MD を共に使用する](using-ado-with-ado-md.md)」を参照してください。

