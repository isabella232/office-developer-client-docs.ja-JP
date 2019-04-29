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
  
進行状況インジケーターを表示するには、呼び出し[imapiprogress:: getflags](imapiprogress-getflags.md)を呼び出して現在のフラグ設定を取得します。 
  
MAPI_TOP_LEVEL フラグが設定されている場合は、次の手順を実行します。
  
1. 操作で処理するアイテムの合計数を変数として設定します。 たとえば、フォルダーの内容をコピーしている場合、この値は、フォルダー内のサブフォルダーとメッセージ数の合計と等しくなります。 
    
2. 変数を1000に設定し、アイテム数で割った値にします。 
    
3. サブオブジェクトの進行状況を表示している場合は、progress オブジェクトの[imapiprogress:: setlimits](imapiprogress-setlimits.md)メソッドを呼び出し、3つのパラメーターに次の値を渡します。 
    
   - lアウト_min_パラメーターを0に設定します。 
    
   - lアウト_max_パラメーターを1000に設定します。 
    
   - lアウト_flags_パラメーターを MAPI_TOP_LEVEL に設定します。 
    
4. 処理するオブジェクトごとに、次の手順を実行します。
    
   1. 呼び出し**imapiprogress:: setlimits** 。3つのパラメーターに対して次の値を渡します。 
      
     - lアウト_min_パラメーターを手順2で設定した変数に、現在のアイテムから1を引いた値を掛けた値に設定します。 
      
     - lアウト_max_パラメーターを、手順2で現在のオブジェクトを乗算した変数セットに設定します。 
      
     - lアウト_flags_パラメーターを0に設定します。 
      
   2. このオブジェクトに対して実行する必要がある処理を実行します。 これがサブオブジェクトで、サブオブジェクトの進行状況を表示する場合は、 _lpprogress_パラメーターの progress オブジェクトへのポインターをメソッドに渡します。 
      
   3. 呼び出し[imapiprogress::P rogress](imapiprogress-progress.md) 、3つのパラメーターに次の値を渡します。 
      
     - _ulvalue_パラメーターに、手順2で現在のオブジェクトを乗算した変数セットを設定します。 
      
     - _ulcount_パラメーターを現在のオブジェクトに設定します。 
      
     - _ultotal_パラメーターを、手順1で設定した変数 (オブジェクトの合計数) に設定します。 
    
MAPI_TOP_LEVEL フラグが設定されていない場合は、次の手順を実行します。
  
1. 状態オブジェクトの[imapiprogress:: getmin](imapiprogress-getmin.md)メソッドを呼び出して、表示の最小値を取得します。 
    
2. 呼び出し[imapiprogress:: getmax](imapiprogress-getmax.md)を使用して、ディスプレイの最大値を取得します。 
    
3. 変数には、処理するオブジェクトの合計数を設定します。 
    
4. 最大値から最小値を減算した結果と同じ変数を設定し、オブジェクトの合計数で除算します。
    
5. 処理するオブジェクトごとに、次の手順を実行します。
    
   1. プロバイダーでサブオブジェクトの進行状況が表示されている場合は、次の3つのパラメーターに対して、 **imapiprogress:: setlimits**を呼び出し、次の値を渡します。 
      
     - lアウト_min_パラメーターを最小値に、現在のアイテムに1を引いた値を、手順4で設定した変数の値で乗算します。 
      
     - lアウト_max_パラメーターを、最小値に、現在の単位に、手順4で設定した変数を掛けた値に設定します。 
      
     - lアウト_flags_パラメーターを0に設定します。 
      
   2. このオブジェクトに対して実行する必要がある処理を実行します。 オブジェクトがサブオブジェクトであり、プロバイダーがサブオブジェクトの進行状況を表示する場合は、 _lpprogress_パラメーターの progress オブジェクトへのポインターをメソッドに渡します。 
      
   3. 呼び出し[imapiprogress::P rogress](imapiprogress-progress.md) 、3つのパラメーターに次の値を渡します。 
      
     - _ulvalue_パラメーターに、手順2で現在のオブジェクトを乗算した変数セットを設定します。 
      
     - _ulcount_パラメーターを0に設定します。 
      
     - _ultotal_パラメーターを0に設定します。 
    
次のコード例は、5つのサブフォルダーを含むフォルダーの内容をコピーする操作のすべてのレベルで進行状況を表示するために必要なロジックを示しています。 
  
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

