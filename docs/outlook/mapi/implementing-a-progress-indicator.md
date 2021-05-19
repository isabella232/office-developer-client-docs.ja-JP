---
title: 進行状況インジケーターの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6972c960705c336aa6ff96d81b48ccbd490a22ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435097"
---
# <a name="implementing-a-progress-indicator"></a>進行状況インジケーターの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントによって開始される操作の多くは、かなりの時間を必要とします。 これらの潜在的に長い操作に対する入力パラメーターの 1 つは [、IMAPIProgress : IUnknown](imapiprogressiunknown.md) インターフェイスを実装するオブジェクトである進行状況オブジェクトへのポインターです。 Progress オブジェクトは進行状況インジケーターの外観と表示を制御し、クライアントと MAPI によって実装されます。 進行状況オブジェクトを実装するかどうかを選択できます。 MAPI 実装は、実装を提供しない場合にサービス プロバイダーが使用できます。 
  
Progress オブジェクトは、次のデータを操作します。
  
- [IMAPIProgress::P rogress](imapiprogress-progress.md)メソッドが呼び出される場合のグローバル最小値は _、ulValue_ パラメーターの値以下にする必要があります。 操作の開始時に  _、ulValue_ はこの最小値と等しくなります。 
    
- **IMAPIProgress::P rogress** メソッドが呼び出される場合のグローバル最大値は _、ulValue_ パラメーター以上にする必要があります。 操作の最後に  _、ulValue_ はこの最大値と等しくなります。 
    
- 進行状況が上位レベルまたは下位レベルのアイテムに対応するかどうかを示すフラグ値。
    
- 操作の進行状況の現在のレベルを示す値。
    
- 合計に対する現在処理されているアイテムの数。
    
- 操作中に処理されるアイテムの総数。
    
最小値と最大値は、操作の開始と終了を数値形式で表します。 最初の最小値には 1、初期最大値には 1000 を使用し [、IMAPIProgress::GetMin](imapiprogress-getmin.md) メソッドと [IMAPIProgress::GetMax](imapiprogress-getmax.md) メソッドのサービス プロバイダーにこれらの値を渡します。 サービス プロバイダーは [、IMAPIProgress::SetLimits を呼び出す際に、これらの値をリセットします](imapiprogress-setlimits.md)。 
  
flags 値は、サービス プロバイダーが他の値を設定する方法を決定するために使用されます。 フラグ値を初期化してMAPI_TOP_LEVEL **SetLimits** を呼び出してサービス プロバイダーがリセットするまで **GetFlags** の実装でこの値を返します。 
  
**SetLimits** メソッドの実装では、各パラメーターのローカル コピー _(lpulMin、lpulMax、lpulFlags)_ を _保存します_。  これらの値は、サービス プロバイダーが GetMin メソッド **、GetMax** メソッド、または **GetFlags** メソッドを呼び出す場合にすぐに使用できる必要があります。  
  
進行状況インジケーターの表示を更新するために、サービス プロバイダーは **IMAPIProgress::P rogress** メソッドを呼び出します。 このメソッドには、値、カウント、および合計の 3 つのパラメーターがあります。 進行状況インジケーターを表示するには、最初のパラメーター  _ulValue_ を使用します。 _ulValue_ パラメーターは進行状況インジケーターであり、操作の開始時にのみグローバル _ulMin_ に、操作の完了時にのみグローバル _ulMax_ に等しくなります。 
  
2 番目と 3 番目のパラメーター  _ulCount_ と  _ulTotal_(使用可能な場合) を使用して、"10 から 5 アイテムが完了しました" などのオプションのメッセージを表示します。 2 番目と 3 番目のパラメーターが 0 に設定されている場合は、進行状況インジケーターを視覚的に変更するかどうかを選択できます。 一部のサービス プロバイダーは、親オブジェクトに対して進行状況を監視するサブオブジェクトを処理している場合に、これらのパラメーターを 0 に設定します。 このような場合は、親オブジェクトが進行状況を報告した場合にのみ表示を変更する必要があります。 一部のサービス プロバイダーは、これらのパラメーターに対して毎回 0 を渡します。 
  

