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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404975"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ値配列のサイズ (バイト単位) を決定し、配列に関連付けられているメモリを検証します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>パラメーター

 _cprop_
  
> [in]  _rgprop_ パラメーターで示される配列内のプロパティの数。 
    
 _rgprop_
  
> [in]サイズを決定するプロパティを定義する [SPropValue](spropvalue.md) 構造体の配列内の範囲へのポインター。 この範囲は必ずしも配列の先頭から始まるとは限りません。 
    
 _pcb_
  
> [out]プロパティ配列のサイズ (バイト単位) へのオプションのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_INVALID_PARAMETER 
  
> プロパティ値配列内の少なくとも 1 つのプロパティに PROP_ID_NULL または PROP_ID_INVALID の識別子が含まれているか、プロパティ配列にプロパティ値がない複数値プロパティが含まれます。
    
## <a name="remarks"></a>注釈

NULL が pcbパラメーターで渡された場合 **、ScCountProps** 関数は通知の配列を検証しますが、カウントは実行されません。 null 以外の値が  _pcb_ で渡された場合 **、ScCountNotifications** 関数は配列のサイズを決定し、原因  _の pcb_ を格納します。 pcb  _パラメーターは_ 、配列全体を格納するのに十分な大きい値である必要があります。 
  
カウント中に **、ScCountProps は** 配列に関連付けられたメモリを検証します。 **ScCountProps は** 、MAPI に関する情報を持つプロパティでのみ動作します。 
  
## <a name="see-also"></a>関連項目



[PropCopyMore](propcopymore.md)

