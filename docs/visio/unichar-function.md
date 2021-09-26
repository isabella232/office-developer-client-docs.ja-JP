---
title: UNICHAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
ms.localizationpriority: medium
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: 数値から Unicode 文字を返します。
ms.openlocfilehash: 8f37e4890b785a0b3557efc1167dc80868f72c7a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603222"
---
# <a name="unichar-function"></a>UNICHAR 関数

数値から Unicode 文字を返します。 
  
## <a name="syntax"></a>構文

UNICHAR (** *number* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |1 ～ 65,535 の整数を指定します。これ以外の数値を指定すると、関数はエラーを返します。  <br/> |
   
## <a name="remarks"></a>注釈

返される文字列の長さは、Unicode 1 文字の長さ (通常の半角 2 文字分) です。 
  
## <a name="example"></a>例

UNICHAR(65) 
  
A (ラテン大文字 A) を返します。 
  

