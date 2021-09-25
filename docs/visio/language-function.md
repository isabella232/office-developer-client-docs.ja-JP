---
title: LANGUAGE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: 異なる言語表現間の比較操作を許可します。 インターネット エンジニアリング タスク フォース言語タグ (BCP 47) の値をロケール ID (LCID) 値に変換する場合に最適です。
ms.openlocfilehash: 319d1a043b43f80accfe5b195a640acaea5a1c52
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554517"
---
# <a name="language-function"></a>LANGUAGE 関数

異なる言語表現間の比較操作を許可します。 インターネット エンジニアリング タスク フォース言語タグ (BCP 47) の値をロケール ID (LCID) 値に変換する場合に最適です。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2013
 
  
## <a name="syntax"></a>構文

 **LANGUAGE** _(_ lcid_or_bcp47 )
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |必須  <br/> |**String** <br/> |言語の LCID または BCP 47 の値。  <br/> |
   
## <a name="return-value"></a>戻り値

整数
  
## <a name="example"></a>例

 `LANGUAGE("en-us")`
  
'1033' の値を返します。
  
 `LANGUAGE("es-es")`
  
'3082' の値を返します。
  

