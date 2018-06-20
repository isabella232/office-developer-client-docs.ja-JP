---
title: LANGUAGE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: さまざまな言語表現との間の比較演算を使用できます。 ロケール id (LCID) の値をインターネット技術標準化委員会言語タグ (BCP 47) の値を変換するためには適しています。
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805675"
---
# <a name="language-function"></a>LANGUAGE 関数

さまざまな言語表現との間の比較演算を使用できます。 ロケール id (LCID) の値をインターネット技術標準化委員会言語タグ (BCP 47) の値を変換するためには適しています。
  
## <a name="version-information"></a>バージョン情報

Visio 2013 のバージョンが追加されます。 
  
## <a name="syntax"></a>構文

 **言語**( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |言語の LCID または BCP 47 の値です。  <br/> |
   
## <a name="return-value"></a>�߂�l

整数型 (Integer)
  
## <a name="example"></a>例

 `LANGUAGE("en-us")`
  
'1033' の値を返します。
  
 `LANGUAGE("es-es")`
  
'3082' の値を返します。
  

