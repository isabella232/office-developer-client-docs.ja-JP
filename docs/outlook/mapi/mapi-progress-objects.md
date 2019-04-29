---
title: MAPI Progress オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 73d905028f8f62ad8cbb9da9b1ad61b8cab1065e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422027"
---
# <a name="mapi-progress-objects"></a>MAPI Progress オブジェクト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
progress オブジェクトのメソッドとデータを使用すると、インジケーターの進捗状況を報告する方法を制御できます。 クライアントまたは MAPI は進行状況オブジェクトを実装していますが、進行状況の表示が正確であることを確認する負担のほとんどは、サービスプロバイダーによって異なります。 progress オブジェクトのメソッドに渡されるパラメーターには、特定の順序と値を指定することで、その正確さを保証できます。
  
progress オブジェクトには、次のパラメーターが渡されます。
  
- フラグのビットマスク。 [imapiprogress:: setlimits](imapiprogress-setlimits.md)で設定し、 [imapiprogress:: getflags](imapiprogress-getflags.md)で取得します。
    
- 最小値 (ローカルおよびグローバル)、 **setlimits**で設定し、imapiprogress で取得します。 [: getmin](imapiprogress-getmin.md)。
    
- **setlimits**で設定され、 [imapiprogress:: getmax](imapiprogress-getmax.md)で取得された最大値 (ローカルおよびグローバル)。
    
- 操作の現在の完了率を示す値[。 imapiprogress::P rogress](imapiprogress-progress.md)に渡されます。
    
- 処理が完了したオブジェクトの数が**進行状況**に渡されます。
    
- 操作に関係しているオブジェクトの合計数のカウント。**進行状況**に渡されます。
    
すべてのサービスプロバイダーは、 **imapiprogress:: getflags**を呼び出して、進行状況の表示処理を開始し、現在のフラグの設定を取得します。 現在、フラグは MAPI_TOP_LEVEL にのみ設定できます。 クライアントと MAPI は、フラグを MAPI_TOP_LEVEL に初期化し、必要に応じてサービスプロバイダーがクリアするようにサービスプロバイダーに依存します。 
  
操作中に最上位レベルのオブジェクトを操作しているときに、flags の値が MAPI_TOP_LEVEL に設定されます。 最上位レベルのオブジェクトは、操作を開始するためにクライアントによって呼び出されるオブジェクトです。 フォルダーコピー操作では、このフォルダーはコピーされます。 フォルダーの削除操作では、このフォルダーは削除されます。 下位レベルのオブジェクトまたはサブオブジェクトを処理する呼び出しを行う場合は、flags 値をクリアします。 フォルダーコピー操作では、サブオブジェクトはコピーされるフォルダー内のサブフォルダーです。 
  
MAPI では、最上位レベルのオブジェクトとサブオブジェクトを MAPI_TOP_LEVEL フラグで区別することができます。このため、操作に関係するすべてのオブジェクトが同じ[imapiprogress](imapiprogressiunknown.md)実装を使用して進行状況を表示することができます。これにより、インジケーターが表示されます。単一の正方向にスムーズに進みます。 MAPI_TOP_LEVEL フラグが設定されているかどうかによって、progress オブジェクトを以降に呼び出すときの他のパラメーターの設定に影響します。 
  
多層演算のすべてのレベルで、進行状況の表示に適切なパラメーター値を設定することが非常に重要な場合があるため、一部のサービスプロバイダーはサブオブジェクトの進行状況を表示しないことを選択しています。 
  
 **サブオブジェクトの進行状況を表示しないようにするには**
  
- サブ操作を処理するには、呼び出しの_lpprogress_パラメーターに NULL を渡します。 たとえば、フォルダーをコピーする場合、これはサブフォルダーの[imapifolder:: copyfolder](imapifolder-copyfolder.md)メソッドへの呼び出しです。 
    
- _lpprogress_パラメーターを解釈する方法を決定する特別なコードを記述します。 _lpprogress_パラメーターに NULL 値を指定すると、クライアントが MAPI 実装を使用して進行状況を表示することがあるため、 _lpprogress_パラメーターを無視するタイミングと呼び出し[のタイミングを決定するために特別なコードが必要になります。imapisupport::D o進捗ダイアログ]](imapisupport-doprogressdialog.md)を選択します。
    
Call **imapiprogress:: setlimits** MAPI_TOP_LEVEL フラグを設定またはクリアし、ローカルおよびグローバルの最小値と最大値を設定します。 flags 設定の値は、progress オブジェクトが最小値と最大値をローカルまたはグローバルに認識するかどうかに影響します。 MAPI_TOP_LEVEL フラグが設定されている場合、これらの値はグローバルと見なされ、操作全体の進行状況を計算するために使用されます。 Progress オブジェクトは、グローバルの最小値を0に、グローバルの最大値を1000に初期化します。 
  
MAPI_TOP_LEVEL が設定されていない場合、最小値と最大値はローカルと見なされ、下位レベルのサブオブジェクトの進行状況を表示するために、プロバイダー内部で使用されます。 Progress オブジェクトは、 **getmin**および**getmin**が呼び出されたときにプロバイダーに返されることができるように、ローカルの最小値と最大値のみを保存します。 
  
value、object count、および object total の各パラメーターは、 **imapiprogress::P rogress**メソッド "に入力します。 value パラメーターは、進行状況のパーセンテージを示す数値です。必須です。 MAPI_TOP_LEVEL フラグが設定されている場合は、オブジェクトの数と合計を渡すこともできます。 クライアントによっては、これらの値を使用して、進行状況インジケーターが表示された「5個のアイテムが10を完了しました」などの語句を表示します。 操作の進行状況は、処理対象となる合計から処理されたアイテムの数として、パーセントまたはパーセンテージとして報告される場合があります。 たとえば、メッセージストアプロバイダーで、10個のフォルダーをコピーするコピー操作を実行している場合は、進行状況インジケーターで、"1 of 10"、"2 of 10"、"3/3" のような語句を表示することによって、ユーザーに追加情報を提供することができます。操作が完了するまで続きます。 
  
## <a name="see-also"></a>関連項目



[MAPI 進行状況インジケーター](mapi-progress-indicators.md)

