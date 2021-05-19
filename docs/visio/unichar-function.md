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
description: 数値から Unicode 文字を返します。
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417582"
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
  

