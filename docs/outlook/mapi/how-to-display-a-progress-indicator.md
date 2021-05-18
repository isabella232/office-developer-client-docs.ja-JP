---
title: 進行状況インジケーターを表示する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7b0ce0ab75ffdce045ccde5bf6ea8a7da046f463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408027"
---
# <a name="display-a-progress-indicator"></a>進行状況インジケーターを表示する
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
進行状況インジケーターを表示するには [、IMAPIProgress::GetFlags](imapiprogress-getflags.md) を呼び出して、現在のフラグ設定を取得します。 
  
このフラグMAPI_TOP_LEVEL設定されている場合は、次の手順を実行します。
  
1. 操作で処理するアイテムの総数に等しい変数を設定します。 たとえば、フォルダーの内容をコピーする場合、この値はフォルダー内のサブフォルダーの数とメッセージの数と等しくなります。 
    
2. 変数を項目数で割った値を 1000 に設定します。 
    
3. サブオブジェクトの進行状況を表示する場合は、progress オブジェクトの [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) メソッドを呼び出し、3 つのパラメーターに次の値を渡します。 
    
   - _lpulMin パラメーターを_ 0 に設定します。 
    
   - _lpulMax パラメーターを_ 1000 に設定します。 
    
   - _lpulFlags_ パラメーターを次の値MAPI_TOP_LEVEL。 
    
4. 処理するオブジェクトごとに、次の手順を実行します。
    
   1. **IMAPIProgress::SetLimits** を呼び出し、3 つのパラメーターに次の値を渡します。 
      
     - 手順 2 の変数セットに  _lpulMin_ パラメーターを設定し、現在の項目から 1 を引いた値を乗算します。 
      
     - _lpulMax パラメーターを_、手順 2 の変数セットに現在のオブジェクトを掛けた値に設定します。 
      
     - _lpulFlags パラメーターを_ 0 に設定します。 
      
   2. このオブジェクトに対して実行する必要がある処理を実行します。 これがサブオブジェクトであり、サブオブジェクトに進行状況を表示する場合は  _、lpProgress_ パラメーターの progress オブジェクトへのポインターをメソッドに渡します。 
      
   3. [IMAPIProgress::P rogress を](imapiprogress-progress.md)呼び出し、3 つのパラメーターに対して次の値を渡します。 
      
     - 手順 2 で設定した変数に、現在のオブジェクトを乗算して  _、ulValue_ パラメーターを設定します。 
      
     - _ulCount パラメーターを_ 現在のオブジェクトに設定します。 
      
     - _ulTotal パラメーターを_、手順 1 の変数セット 、オブジェクトの総数に設定します。 
    
このフラグMAPI_TOP_LEVEL設定されていない場合は、次の手順を実行します。
  
1. 進行状況オブジェクトの [IMAPIProgress::GetMin](imapiprogress-getmin.md) メソッドを呼び出して、表示の最小値を取得します。 
    
2. [IMAPIProgress::GetMax](imapiprogress-getmax.md)を呼び出して、表示の最大値を取得します。 
    
3. 処理するオブジェクトの総数に等しい変数を設定します。 
    
4. 最大値から最小値を減算し、オブジェクトの総数で割った結果と等しい変数を設定します。
    
5. 処理するオブジェクトごとに、次の手順を実行します。
    
   1. プロバイダーがサブオブジェクトの進行状況を表示している場合は **、IMAPIProgress::SetLimits** を呼び出し、3 つのパラメーターに次の値を渡します。 
      
     - _lpulMin パラメーターに_、手順 4 で設定した変数に現在の項目から 1 を掛けた最小値を設定します。 
      
     - _lpulMax パラメーターに_、手順 4 で設定した変数を乗算した現在の単位を加えた最小値を設定します。 
      
     - _lpulFlags パラメーターを_ 0 に設定します。 
      
   2. このオブジェクトに対して実行する必要がある処理を実行します。 オブジェクトがサブオブジェクトで、プロバイダーがサブオブジェクトの進行状況を表示する場合は  _、lpProgress_ パラメーターの progress オブジェクトへのポインターをメソッドに渡します。 
      
   3. [IMAPIProgress::P rogress を](imapiprogress-progress.md)呼び出し、3 つのパラメーターに対して次の値を渡します。 
      
     - 手順 2  _で現在_ のオブジェクトを乗算して、ulValue パラメーターを変数セットに設定します。 
      
     - _ulCount パラメーターを_ 0 に設定します。 
      
     - _ulTotal パラメーターを_ 0 に設定します。 
    
次のコード例は、5 つのサブフォルダーを含むフォルダーの内容をコピーする操作のすべてのレベルで進行状況を表示するために必要なロジックを示しています。 
  
```cpp
lpProgress->GetFlags (lpulFlags);
ulFlags = *lpulFlags;
/* The folder in charge of the display. It contains 5 subfolders. */
if (ulFlags & MAPI_TOP_LEVEL)
{
    ulItems = 5                         // 5 subfolders in this folder
    ulScale = (ulMax / ulItems)         // 200 because ulMax = 1000
    lpProgress->SetLimits(0, ulMax, MAPI_TOP_LEVEL)
    for (i = 1; i <= ulItems; i++)      // for each subfolder to copy
    {
        lpProgress->SetLimits( (i - 1) * ulScale, i * ulScale, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        lpProgress->Progress( i * ulScale, i, ulItems)
    }
}
else
/* One of the subfolders to be copied. It contains 3 messages. */
{
    lpProgress->GetMin(&ulMin);
    lpProgress->GetMax(&ulMax);
    ulItems = 3;
    ulDelta = (ulMax - ulMin) / ulItems;
    for (i = 1; i <= ulItems; i++)
    {
        lpProgress->SetLimits(ulMin + (i - 1) * ulDelta,
                              ulMin + i * ulDelta, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        /* Pass 0 for ulCount and ulTotal because this is not the */
        /* top-level display, and that information is unavailable  */
        lpProgress->Progress( i * ulDelta, 0, 0)
    }
}
 
```

## <a name="see-also"></a>関連項目

- [MAPI 進行状況インジケーター](mapi-progress-indicators.md)

