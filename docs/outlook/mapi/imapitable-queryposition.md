---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415664"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
小数値に基づいて、カーソルの現在のテーブル行の位置を取得します。
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>パラメーター

 _lの行_
  
> 読み上げ現在の行の番号へのポインター。 行番号は0から始まります。表の最初の行は0になります。 
    
 _lアウト分子_
  
> 読み上げテーブルの位置を識別する分数の分子へのポインター。
    
 _lアウト分母_
  
> 読み上げテーブルの位置を識別する分数の分母へのポインター。 _lアウト分母_パラメーターを0にすることはできません。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メソッドは、 _lな行_の有効な値、l出た_分子_、および_lアウト分母_を返しました。
    
## <a name="remarks"></a>注釈

**IMAPITable:: queryposition**メソッドは、現在の行の位置を決定し、現在の行の数と、テーブルの最後までの相対位置を示す小数値を返します。 MAPI は、現在の行を読み取る次の行として定義します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_lアウト分母_パラメーターのテーブル内の行の正確な数を返す必要はありません。近似値になることがあります。 
  
現在の行を特定できない場合は、 _lアウト row_で値0xffffffff を返します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**queryposition**を使用して、スクロールバーのスクロールボックスを配置できます。 たとえば、100行を含むテーブルで、 **queryposition**が l出_分子_パラメーターで75の値を返し、l出_分母_パラメーターで100を返した場合は、スクロールボックス__ を次のように配置できます。をスクロールバーの上方向に移動します。 
  
テーブル内の行の数として、 _lアウト分母_の値に依存しないようにしてください。 **queryposition**は、カーソルが置かれている正確な行を常に識別することはできません。 
  
**queryposition**の呼び出しでは、特に、大きな分類されたテーブルの場合は、大量のメモリが関係することがあります。 lの_行_パラメーターが0xffffffff に設定されている場合、 **queryposition**が現在の行を特定するために必要なメモリの量が多すぎます。 [IMAPITable:: seekrowapprox](imapitable-seekrowapprox.md)メソッドを呼び出して、 _lpulnumerator_パラメーターと_lアウト分母_パラメーターで識別される行にテーブルを配置します。 ただし、メモリが係数で**** ない場合は、同じ行**queryposition**が現在の位置として設定されていると常に期待してはいけません。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

