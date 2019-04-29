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
  
クライアントによって開始される操作の多くには、かなりの時間がかかります。 このような長い時間がかかる可能性のある操作への入力パラメーターの1つは、progress オブジェクトへのポインターです。これは、 [imapiprogress: IUnknown](imapiprogressiunknown.md)インターフェイスを実装するオブジェクトです。 progress オブジェクトは、進行状況インジケーターの表示と表示を制御し、クライアントと MAPI で実装されます。 progress オブジェクトを実装するかどうかを選択できます。 実装を提供しない場合は、サービスプロバイダーが MAPI 実装を使用できるようになります。 
  
Progress オブジェクトは、次のデータを使用して機能します。
  
- [imapiprogress::P rogress](imapiprogress-progress.md)メソッドが呼び出されたときに、 _ulvalue_パラメーターの値以下である必要がある、グローバルな最小値。 操作の開始時に、 _ulvalue_はこの最小値と等しくなります。 
    
- **imapiprogress::P rogress**メソッドが呼び出されるときに、 _ulvalue_パラメーター以上である必要があるグローバル最大値。 操作の終了時に、 _ulvalue_はこの最大値と等しくなります。 
    
- 進捗状況が上位または下位レベルのアイテムに対応するかどうかを示すフラグ値。
    
- 操作の現在の進行状況レベルを示す値。
    
- 現在処理されているアイテムの総数を基準としたアイテムの数。
    
- 操作中に処理されるアイテムの合計数。
    
最小値と最大値は、操作の開始と終了を数値形式で表します。 最初の最小値には1、最大値には1000を使用します。これらの値は、 [imapiprogress:: getmin](imapiprogress-getmin.md)および[imapiprogress:: getmin](imapiprogress-getmax.md)メソッドのサービスプロバイダーに渡されます。 サービスプロバイダー[は、imapiprogress:: setlimits](imapiprogress-setlimits.md)を呼び出したときに、これらの値をリセットします。 
  
flags 値は、サービスプロバイダーが他の値をどのように設定するかを決定するために使用されます。 flags 値を MAPI_TOP_LEVEL に初期化し、 **getflags**の実装で、 **setlimits**を呼び出してサービスプロバイダーがリセットするまでこの値を返します。 
  
**setlimits**メソッドの実装では、各パラメーターのローカルコピーを_lルー min_、 _l出 max_、lアウトの各_フラグ_で保存します。 これらの値は、サービスプロバイダーが**getmin**、 **getmin**、または**getmin**メソッドを呼び出すときにすぐに使用できるようにする必要があります。 
  
進行状況インジケーターの表示を更新するために、サービスプロバイダーは imapiprogress を呼び出します。 **:P rogress** method。 このメソッドには、値、数、合計という3つのパラメーターがあります。 最初のパラメーター _ulvalue_を使用して進行状況インジケーターを表示します。 _ulvalue_パラメーターは進行状況インジケーターで、操作の開始時にグローバル_ulvalue_のみになり、操作が完了したときにのみグローバル_ulvalue_に等しくなります。 
  
2番目および3番目のパラメーター [ _ulcount_ ] および [ _ulcount_] を使用して、"5 個のアイテムが完了しました" のようなオプションのメッセージを表示します (使用可能な場合)。 2番目と3番目のパラメーターが0に設定されている場合は、進行状況インジケーターを視覚的に変更するかどうかを選択できます。 一部のサービスプロバイダーでは、このパラメーターを0に設定して、進行状況が親オブジェクトに対して監視されているサブオブジェクトを処理していることを示します。 このような状況では、親オブジェクトが進捗状況を報告する場合にのみ、表示を変更することをお勧めします。 一部のサービスプロバイダーでは、これらのパラメーターに対して常に0が渡されます。 
  

