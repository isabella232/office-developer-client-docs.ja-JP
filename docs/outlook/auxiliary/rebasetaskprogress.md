---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: 列挙体は、単独の予定の再配置の進行状況を報告します。
ms.openlocfilehash: 4219ab1d59b596bebbe3ced03651716b04b51f81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799585"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

列挙体は、単独の予定の再配置の進行状況を報告します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |tzmovelib.h  <br/> |
|によって実装されます。  <br/> |MAPI クライアント アプリケーション  <br/> |
|によって呼び出されます。  <br/> |Outlook の再配置オブジェクト  <br/> |
|ポインターの型。  <br/> |**PFNREBASETASKPROGRESS** tzmovelib.h で定義されています。  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a>パラメーター

_ulMin_
  
> [in]処理中の予定の範囲の下限です。 一般的には、ゼロです。
    
_ulMax_
  
> [in]処理中の予定の範囲の上限です。 これは、通常、処理中の予定表フォルダー内のアイテムの数です。
    
_ulCur_
  
> [in]処理されている現在の項目。
    
_State_
  
> [in]処理されている項目のステータスを示す値。 **REBASE_APPT_STATE**列挙体は、tzmovelib.h で定義されます。  _状態_は、次の値のいずれかです。 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** -スキャンし、項目を確認します。 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** -スキャンの項目が見つかったとします。 
    
   - **REBASE_APPT_STATE_BEGIN** -修正および項目を開始します。 
    
   - **REBASE_APPT_STATE_REBASING** -修正および項目を調整します。 
    
   - **REBASE_APPT_STATE_SENDING** -修正し、会議の更新を送信します。 
    
   - **REBASE_APPT_STATE_DONE** : 解決であり、項目を実行します。 
    
_pRowCur_
  
> [in]スキャンまたは固定されている項目を説明する**[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアント アプリケーションは、項目の処理を追跡するためにこの関数を実装します。 
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

