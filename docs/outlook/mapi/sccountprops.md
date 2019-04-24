---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351318"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ値の配列のサイズをバイト単位で指定し、配列に関連付けられているメモリを検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>パラメーター

 _cprop_
  
> 順番_rgprop_パラメーターによって示される、配列内のプロパティの数。 
    
 _rgprop_
  
> 順番サイズを決定するプロパティを定義する[spropvalue](spropvalue.md)構造体の配列内の範囲へのポインター。 この範囲は、必ずしも配列の先頭から開始することはできません。 
    
 _設計_
  
> 読み上げ(オプション) プロパティ配列のサイズ (バイト単位) のポインターです。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_INVALID_PARAMETER 
  
> プロパティ値配列の少なくとも1つのプロパティに PROP_ID_NULL または PROP_ID_INVALID の識別子があるか、プロパティ配列にプロパティ値を持たない複数値プロパティが含まれています。
    
## <a name="remarks"></a>解説

_pcb_パラメーターで NULL が渡された場合、 **sccountprops**関数は通知の配列を検証しますが、カウントは行われません。 非 null 値が_pcb_で渡された場合、 **sccountnotifications**関数は配列のサイズを決定し、原因となった_pcb_を格納します。 _pcb_パラメーターは、配列全体を格納するのに十分な大きさである必要があります。 
  
カウントすると、 **sccountprops**は配列に関連付けられているメモリを検証します。 **sccountprops**は、どの MAPI が情報を持っているかに関するプロパティでのみ動作します。 
  
## <a name="see-also"></a>関連項目



[PropCopyMore](propcopymore.md)

