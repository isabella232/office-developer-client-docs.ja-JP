---
title: UNICHAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: 番号から Unicode 文字を返します。
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806727"
---
# <a name="unichar-function"></a>UNICHAR 関数

番号から Unicode 文字を返します。 
  
## <a name="syntax"></a>構文

UNICHAR (* **番号** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**Integer** <br/> |1 ～ 65,535 の整数を指定します。これ以外の数値を指定すると、関数はエラーを返します。  <br/> |
   
## <a name="remarks"></a>注釈

返される文字列の長さは、Unicode 1 文字の長さ (通常の半角 2 文字分) です。 
  
## <a name="example"></a>例

UNICHAR(65) 
  
(ラテン大文字 A) を返します。 
  

