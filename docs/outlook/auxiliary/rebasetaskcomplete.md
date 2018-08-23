---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: 予定の再配置の完了を報告します。
ms.openlocfilehash: 735d875b4151c86103a1ac0378bd33b84de64997
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799589"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

予定の再配置の完了を報告します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |tzmovelib.h  <br/> |
|によって実装されます。  <br/> |MAPI クライアント アプリケーション  <br/> |
|によって呼び出されます。  <br/> |Outlook の再配置オブジェクト  <br/> |
|ポインターの型。  <br/> |**PFNREBASETASKCOMPLETE** tzmovelib.h で定義されています。  <br/> |
   
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
  
> [in]処理された行です。 このインデックスは、 [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)に渡される**[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** 構造体を指します。
    
_pRowCur_
  
> in] 項目が処理されたことを説明する**[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。 
    
_hrResult_
  
> [in]再配置操作の結果を示す**HRESULT** 。 
    
_fModified_
  
> [in]アイテムが変更されたかどうかを指定します。
    
_fSentUpdate_
  
> [in]指定送信された会議がメッセージを更新するかどうか。 
    
_pError_
  
> [in]拡張エラー情報を含む**MAPIERROR**構造体へのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアント アプリケーションは、項目の更新の完了を追跡するためにこの関数を実装します。 
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

