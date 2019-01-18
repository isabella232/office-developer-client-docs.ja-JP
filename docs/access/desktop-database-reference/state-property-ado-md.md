---
title: State プロパティ (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702447"
---
# <a name="state-property-ado-md"></a>State プロパティ (ADO MD)


**適用されます**Access 2013、Office 2013。

セルセットの現在の状態を示します。

## <a name="return-values"></a>戻り値

**Cellset** オブジェクトの現在の状態を示す長整数型 ( [Long](cellset-object-ado-md.md) ) の値を取得します。値の取得のみが可能です。有効な値は、 **adStateClosed** (0) および **adStateOpen** (1) です。

## <a name="remarks"></a>解説

[ObjectStateEnum](objectstateenum.md) 定数の名前を使用するには、プロジェクトで ADO タイプ ライブラリが参照されている必要があります。詳細については、「 [ADO と ADO MD を共に使用する](using-ado-with-ado-md.md)」を参照してください。

