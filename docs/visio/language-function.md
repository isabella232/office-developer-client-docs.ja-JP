---
title: LANGUAGE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: 異なる言語表現間での比較操作を可能にします。 これは、インターネットエンジニアリングのタスクフォースの言語タグ (BCP 47) の値をロケール id (LCID) の値に変換するために最適です。
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424754"
---
# <a name="language-function"></a>LANGUAGE 関数

異なる言語表現間での比較操作を可能にします。 これは、インターネットエンジニアリングのタスクフォースの言語タグ (BCP 47) の値をロケール id (LCID) の値に変換するために最適です。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **言語**( _lcid_or_bcp47_)
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |必須  <br/> |**String** <br/> |言語の LCID または BCP 47 の値。  <br/> |
   
## <a name="return-value"></a>戻り値

整数
  
## <a name="example"></a>例

 `LANGUAGE("en-us")`
  
' 1033 ' の値を返します。
  
 `LANGUAGE("es-es")`
  
' 3082 ' の値を返します。
  

