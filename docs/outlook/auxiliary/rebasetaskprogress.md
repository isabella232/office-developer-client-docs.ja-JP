---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: 予定の列挙と再適用の進行状況を報告します。
ms.openlocfilehash: 8ea71e8a76baf8b7f69afa90ac9f0c06c1a64a1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614312"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

予定の列挙と再適用の進行状況を報告します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |tzmovelib.h  <br/> |
|実装元:  <br/> |MAPI クライアント アプリケーション  <br/> |
|呼び出し元:  <br/> |Outlookの再バーズ  <br/> |
|ポインターの種類:  <br/> |tzmovelib.h で定義されている **PFNREBASETASKPROGRESS**  <br/> |
   
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
  
> [in]処理される予定の範囲の低い端。 通常は 0 です。
    
_ulMax_
  
> [in]処理される予定の範囲の高端。 これは通常、処理される予定表フォルダー内のアイテムの数です。
    
_ulCur_
  
> [in]現在処理されているアイテム。
    
_State_
  
> [in]処理されるアイテムの状態を示す値。 列挙型 **REBASE_APPT_STATE** tzmovelib.h で定義されます。  _State_ は、次のいずれかの値です。 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** —アイテムをスキャンして調べる。 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** — アイテムをスキャンして見つかりました。 
    
   - **REBASE_APPT_STATE_BEGIN** —アイテムの固定と開始。 
    
   - **REBASE_APPT_STATE_REBASING** —アイテムの固定と調整。 
    
   - **REBASE_APPT_STATE_SENDING** —会議の更新プログラムを修正して送信します。 
    
   - **REBASE_APPT_STATE_DONE** —アイテムを修正して完了します。 
    
_pRowCur_
  
> [in]スキャンまたは修正されるアイテムを記述する **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアント アプリケーションは、アイテム処理を追跡するためにこの関数を実装します。 
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

