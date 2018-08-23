---
title: 進行状況インジケーターを表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 62549cbeea0044ceee8aa2e704b8a9bc271b7e8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564494"
---
# <a name="display-a-progress-indicator"></a>進行状況インジケーターを表示します。
 
**適用されます**: Outlook 2013 |Outlook 2016 
  
進行状況インジケーターを表示するには、現在のフラグの設定を取得するために[IMAPIProgress::GetFlags](imapiprogress-getflags.md)を呼び出します。 
  
MAPI_TOP_LEVEL フラグが設定されている場合は、次の手順に行います。
  
1. 操作で処理する項目の合計数を変数に格納に設定します。 たとえば、フォルダーの内容をコピーする場合この値は、フォルダー内のサブフォルダーの数とメッセージの数と等しいのようになります。 
    
2. 1000 の項目の数で割った値を変数に格納を設定します。 
    
3. サブオブジェクトの進行状況を表示する場合、進行中のオブジェクトの[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドを呼び出すし、次の 3 つのパラメーターの値を渡します。 
    
   - _LpulMin_パラメーターを 0 に設定します。 
    
   - _LpulMax_パラメーターを 1000 に設定します。 
    
   - _LpulFlags_パラメーターを MAPI_TOP_LEVEL に設定します。 
    
4. 各オブジェクトを処理するには、次の手順を行います。
    
   1. **IMAPIProgress::SetLimits**を呼び出すし、次の 3 つのパラメーターの値を渡します。 
      
     - 変数から 1 を引いた現在の項目を掛けた値 2 の手順で設定するには、 _lpulMin_パラメーターを設定します。 
      
     - 手順 2 の現在のオブジェクトを掛けた値に設定する変数には、 _lpulMax_パラメーターを設定します。 
      
     - _LpulFlags_パラメーターを 0 に設定します。 
      
   2. このオブジェクトに対するすべての処理を行う必要がありますを実行します。 サブオブジェクト、サブオブジェクトの進行状況を表示する場合、メソッドの_lpProgress_パラメーターで進行中のオブジェクトへのポインターを渡します。 
      
   3. [IMAPIProgress::Progress](imapiprogress-progress.md)を呼び出すし、次の 3 つのパラメーターの値を渡します。 
      
     - 手順 2 の現在のオブジェクトを掛けた値に設定する変数には、 _ulValue_パラメーターを設定します。 
      
     - 現在のオブジェクトには、 _ulCount_パラメーターを設定します。 
      
     - 手順 1 のオブジェクトの合計数を設定する変数には、 _ulTotal_パラメーターを設定します。 
    
MAPI_TOP_LEVEL フラグが設定されていない場合は、次の手順に行います。
  
1. 表示の最小値を取得するために、実行中のオブジェクトの[IMAPIProgress::GetMin](imapiprogress-getmin.md)メソッドを呼び出します。 
    
2. 表示の最大値を取得するために[IMAPIProgress::GetMax](imapiprogress-getmax.md)を呼び出します。 
    
3. 変数に格納を処理するオブジェクトの合計数に設定します。 
    
4. 最大値から最小値を減算し、オブジェクトの合計数で除算して結果を変数に格納を設定します。
    
5. 各オブジェクトを処理するには、次の手順を行います。
    
   1. プロバイダーには、サブオブジェクトの進行状況が表示されている場合**IMAPIProgress::SetLimits**を呼び出すし、次の 3 つのパラメーターの値を渡します。 
      
     - _LpulMin_パラメーターを設定すると、最小値は、手順 4 で設定する変数を乗算した値 1 を引いた数値です。 
      
     - _LpulMax_パラメーターを設定すると、最小値と現在の単位を手順 4 で設定する変数を乗算します。 
      
     - _LpulFlags_パラメーターを 0 に設定します。 
      
   2. このオブジェクトに対するすべての処理を行う必要がありますを実行します。 オブジェクトには、サブオブジェクトと、プロバイダーには、下位オブジェクトの進行状況が表示されます、メソッドの_lpProgress_パラメーターで進行中のオブジェクトにポインターを渡します。 
      
   3. [IMAPIProgress::Progress](imapiprogress-progress.md)を呼び出すし、次の 3 つのパラメーターの値を渡します。 
      
     - _UlValue_パラメーターを手順 2 の現在のオブジェクトを掛けた値に設定された変数に設定します。 
      
     - _UlCount_パラメーターを 0 に設定します。 
      
     - _UlTotal_パラメーターを 0 に設定します。 
    
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

- [MAPI の進捗状況](mapi-progress-indicators.md)

