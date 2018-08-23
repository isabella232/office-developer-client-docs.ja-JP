---
title: 進行状況インジケーターの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1a359ec413da91b3e2819978e80ea0a921f6b245
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587125"
---
# <a name="implementing-a-progress-indicator"></a>進行状況インジケーターの実装

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
多くのクライアントによって開始された操作により、かなりの時間がかかります。 進行中のオブジェクトへのポインターは、これらの可能性のある時間のかかる操作への入力パラメーターの 1 つ-を実装するオブジェクトの[IMAPIProgress: IUnknown](imapiprogressiunknown.md)インタ フェースです。 進行状況オブジェクトでは、進行状況インジケーターの表示と外観を制御してと MAPI クライアントによって実装されます。 進行中のオブジェクトを実装するかどうかを選択することができます。 MAPI 実装は、実装を提供するように選択する場合に使用するサービス プロバイダーを使用できます。 
  
進行中のオブジェクトは、次のどのデータを扱います。
  
- グローバル最小値、 [IMAPIProgress::Progress](imapiprogress-progress.md)メソッドが呼び出されるは、 _ulValue_パラメーターの値以下である必要があります。 操作の先頭には、 _ulValue_をこの最小値と等しくなります。 
    
- **IMAPIProgress::Progress**メソッドが呼び出されると、必要があります以上の_ulValue_パラメーターに値をグローバルな最大値です。 操作の最後に、 _ulValue_がこの最大値に等しくなります。 
    
- フラグは、上に進行状況が対応しているかどうかを示す値または項目レベルを下げます。
    
- 操作の進行中の現在のレベルを示す値。
    
- 合計を基準にして現在処理されたアイテムの数です。
    
- 操作中に処理する品目の合計数です。
    
最小値と最大値は、先頭と末尾の数値形式での操作を表します。 初期の最小値と、 [IMAPIProgress::GetMin](imapiprogress-getmin.md)メソッドと[IMAPIProgress::GetMax](imapiprogress-getmax.md)メソッドのサービス プロバイダーにこれらの値を渡すこと、初期の最大値の 1000 の 1 を使用します。 サービス プロバイダーは、 [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)を呼び出すときに、これらの値をリセットします。 
  
フラグ値は、他の値を設定する必要がある方法を決定するのには、サービス プロバイダーによって使用されます。 MAPI_TOP_LEVEL するフラグ値を初期化し、 **SetLimits**を呼び出すことにより、サービス プロバイダーがリセットするまで、 **GetFlags**の実装では、この値を返します。 
  
**SetLimits**メソッドの実装で、各パラメーターのローカル コピーを保存します: _lpulMin_、 _lpulMax_、および_lpulFlags_。 これらの値は、サービス プロバイダーは、 **GetMin**、 **GetMax**、または**GetFlags**メソッドを呼び出すと、すぐに利用できることがあります。 
  
進行状況インジケーターの表示を更新するには、サービス プロバイダーは、 **IMAPIProgress::Progress**メソッドを呼び出します。 このメソッドを次の 3 つのパラメーター: 値、カウント、および合計。 進行状況インジケーターを表示するには、最初のパラメーターでは、 _ulValue_を使用します。 _UlValue_パラメーターでは、進行状況のインジケーターし、 _ulMin_グローバル操作の先頭に、かつ、操作の完了時にのみグローバルの_ulMax_と同じになります。 
  
「5 アイテム 10 個が完了した」などのオプションのメッセージを表示するのには、利用可能な場合は、2 番目と 3 番目のパラメーター、 _ulCount_ _ulTotal_を使用してください。 2 番目と 3 番目のパラメーターを 0 に設定されている場合は、進行状況を視覚的に変更するかどうかを選択できます。 サービス プロバイダーによっては、サブオブジェクトの進行状況は、親オブジェクトを基準にして処理することを示すためにゼロにこれらのパラメーターを設定します。 このような状況は、親オブジェクトの進行状況を報告する場合にのみ、表示を変更します。 サービス プロバイダーによっては、毎回これらのパラメーターに 0 を渡します。 
  

