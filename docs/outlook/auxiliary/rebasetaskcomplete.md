---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: 予定の再処理の完了を報告します。
ms.openlocfilehash: 49061cf21f4a6ffd3218bac2470a1afc6e2ebf81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614333"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

予定の再処理の完了を報告します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |tzmovelib.h  <br/> |
|実装元:  <br/> |MAPI クライアント アプリケーション  <br/> |
|呼び出し元:  <br/> |Outlookの再バーズ  <br/> |
|ポインターの種類:  <br/> |tzmovelib.h で定義されている **PFNREBASETASKCOMPLETE**  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a>パラメーター

_ulRowIndex_
  
> [in]処理された行。 このインデックスは [、IOlkApptRebaser::BeginRebaseAppointments に渡される SRowSet 構造体を参照します](iolkapptrebaser-beginrebaseappointments.md)。 **[](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)**
    
_pRowCur_
  
> in] 処理されたアイテムを記述する **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。 
    
_hrResult_
  
> [in]再バーズ操作の結果を示す **HRESULT。** 
    
_fModified_
  
> [in]アイテムが変更されたかどうかを指定します。
    
_fSentUpdate_
  
> [in]会議の更新メッセージが送信されたかどうかを指定します。 
    
_pError_
  
> [in]拡張エラー情報 **を持つ MAPIERROR** 構造体へのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアント アプリケーションは、アイテムの更新の完了を追跡するためにこの関数を実装します。 
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

