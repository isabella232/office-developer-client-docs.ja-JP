---
title: IFERROR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 232fa528-2375-90be-8e18-7a064ce1345e
description: エラーが発生すると評価されない場合は、1 次の式の評価結果を返します。 それ以外の場合、代替式の評価結果を返します。
ms.openlocfilehash: 5915d0cb8219ced190c6b53043188c96d2b56b5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805570"
---
# <a name="iferror-function"></a>IFERROR 関数

エラーが発生すると評価されない場合は、1 次の式の評価結果を返します。 それ以外の場合、代替式の評価結果を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

IFERROR (* **式** *、* **代替式** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _プライマリ式_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |評価する最初の式。  <br/> |
| _代替式_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |一次式がエラーに評価される場合に評価する代替式。  <br/> |
   
### <a name="return-value"></a>戻り値

可変型 (Varies)
  

