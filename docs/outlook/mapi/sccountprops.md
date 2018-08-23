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
ms.openlocfilehash: ee004bdfb8d13537fd8823225f155223ebc76ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583352"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロパティ値の配列のバイト単位のサイズを決定し、配列に関連付けられているメモリを確認します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>パラメーター

 _cprop_
  
> [in]_Rgprop_パラメーターで指定された配列内のプロパティの数です。 
    
 _rgprop_
  
> [in][SPropValue](spropvalue.md)構造体のサイズを確認するプロパティを定義する配列内の範囲へのポインター。 この範囲は、配列の先頭に必ずしも起動しません。 
    
 _pcb_
  
> [out]ポインターをプロパティの配列のバイト単位のサイズを指します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_INVALID_PARAMETER 
  
> PROP_ID_NULL または PROP_ID_INVALID の識別子のプロパティ値の配列内の少なくとも 1 つのプロパティまたはプロパティ配列には、複数値を持つプロパティ値のないプロパティが含まれています。
    
## <a name="remarks"></a>注釈

_Pcb_のパラメーターに NULL が渡されると、通知の配列を検証する**ScCountProps**関数が、カウントは行われません。 **ScCountNotifications**関数が配列のサイズを決定し、原因を格納する_pcb_の null 以外の値が渡された場合_pcb_です。 _Pcb_のパラメーターは、配列全体を格納できる大きさである必要があります。 
  
それがカウントと**ScCountProps**は、配列に関連付けられているメモリを検証します。 **ScCountProps**は、MAPI に関する情報を持つプロパティでのみ有効です。 
  
## <a name="see-also"></a>関連項目



[PropCopyMore](propcopymore.md)

