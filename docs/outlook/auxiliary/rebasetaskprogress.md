---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: 予定の列挙およびリベースの進行状況を報告します。
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326454"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

予定の列挙およびリベースの進行状況を報告します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |、tzmovelib.h  <br/> |
|実装元:  <br/> |MAPI クライアントアプリケーション  <br/> |
|呼び出し元:  <br/> |Outlook のリベース/再配置オブジェクト  <br/> |
|ポインターの種類:  <br/> |、tzmovelib.h で定義されている**PFNREBASETASKPROGRESS**  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a>パラメーター

_ulmin_
  
> 順番処理されている予定の範囲の下限。 通常は0になります。
    
_ulmax_
  
> 順番処理されている予定の範囲の上限です。 通常は、処理されている予定表フォルダー内のアイテムの数です。
    
_ulcur_
  
> 順番処理されている現在のアイテムです。
    
_State_
  
> 順番処理されているアイテムの状態を示す値。 列挙**REBASE_APPT_STATE**は、tzmovelib.h で定義されています。  _State_ は、次のいずれかの値です。 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** -アイテムをスキャンし、検査します。 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** —アイテムをスキャンして検出しました。 
    
   - **REBASE_APPT_STATE_BEGIN** —アイテムを修正して開始します。 
    
   - **REBASE_APPT_STATE_REBASING** —アイテムを修正し、調整します。 
    
   - **REBASE_APPT_STATE_SENDING** —会議の更新を修正し、送信します。 
    
   - **REBASE_APPT_STATE_DONE** —アイテムを修正して実行します。 
    
_pRowCur_
  
> 順番スキャンまたは固定されているアイテムを記述する**[srow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解説

[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアントアプリケーションは、この関数を実装してアイテム処理を追跡します。 
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

