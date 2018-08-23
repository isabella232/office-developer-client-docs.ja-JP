---
title: CALLOUTTARGETREF 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: 引き出し図形の対象図形のシート参照を返します。
ms.openlocfilehash: 1b0cb7c6737a810a0ade65f19afaff7bb4b9f616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804927"
---
# <a name="callouttargetref-function"></a>CALLOUTTARGETREF 関数

引き出し図形の対象図形のシート参照を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

CALLOUTTARGETREF()!
  
### <a name="return-value"></a>戻り値

シェイプシート参照
  
## <a name="remarks"></a>注釈

図形が吹き出し図形でない場合、または接続先の図形に関連付けされていない場合は、CALLOUTTARGETREF は、#REF を返します。
  
## <a name="example"></a>例

CALLOUTTARGETREF()!Height 
  
引き出しに関連付けられた図形の [Height] セルの値を返します。 
  

