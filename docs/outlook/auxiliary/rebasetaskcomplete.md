---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: 予定のリベースの完了を報告します。
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328323"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

予定のリベースの完了を報告します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |、tzmovelib.h  <br/> |
|実装元:  <br/> |MAPI クライアントアプリケーション  <br/> |
|呼び出し元:  <br/> |Outlook のリベース/再配置オブジェクト  <br/> |
|ポインターの種類:  <br/> |、tzmovelib.h で定義されている**PFNREBASETASKCOMPLETE**  <br/> |
   
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

_ulrowindex_
  
> 順番処理された行です。 このインデックスは、 [IOlkApptRebaser:: beginrebaseappointments](iolkapptrebaser-beginrebaseappointments.md)に渡される**[srowset](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** 構造を参照します。
    
_pRowCur_
  
> in] 処理されたアイテムを説明する**[srow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。 
    
_hrresult_
  
> 順番リベース操作の結果を示す**HRESULT** 。 
    
_fmodified_
  
> 順番アイテムが変更されたかどうかを指定します。
    
_f文の更新_
  
> 順番会議更新メッセージが送信されたかどうかを指定します。 
    
_の場合_
  
> 順番拡張エラー情報を含む**MAPIERROR**構造体へのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解説

[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアントアプリケーションは、この関数を実装して、アイテムの更新の完了を追跡します。 
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

