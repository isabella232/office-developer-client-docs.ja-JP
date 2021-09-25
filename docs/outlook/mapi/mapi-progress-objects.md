---
title: MAPI 進行状況オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f47abaa8892d6deadbe89eb6c05a152c84f7377f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579573"
---
# <a name="mapi-progress-objects"></a>MAPI 進行状況オブジェクト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
progress オブジェクトのメソッドとデータを使用すると、インジケーターが進行状況を報告する方法を制御できます。 クライアントまたは MAPI は progress オブジェクトを実装しますが、進行状況表示の正しさを確保する負担の大部分は、サービス プロバイダーに当たっています。 進行状況オブジェクト メソッドに渡されるパラメーターの特定の順序と値を指定することで、精度を保証できます。
  
進行状況オブジェクトには、次のパラメーターが渡されます。
  
- [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)で設定され[、IMAPIProgress::GetFlags](imapiprogress-getflags.md)で取得されるフラグのビットマスク。
    
- 最小値 (ローカルとグローバル) は **、SetLimits** で設定され [、IMAPIProgress::GetMin で取得されます](imapiprogress-getmin.md)。
    
- 最大値 (ローカルとグローバル) を **SetLimits** で設定し [、IMAPIProgress::GetMax で取得します](imapiprogress-getmax.md)。
    
- [IMAPIProgress::P rogress](imapiprogress-progress.md)に渡される、操作の現在の完了率を示す値。
    
- これまでに処理されたオブジェクトの数を Progress に渡 **します**。
    
- Progress に渡される、操作に関連するオブジェクトの総数の **カウント** です。
    
すべてのサービス プロバイダーは **、IMAPIProgress::GetFlags** を呼び出して進行状況表示処理を開始し、現在のフラグ設定を取得します。 現在、フラグを設定できるのは、次のMAPI_TOP_LEVEL。 クライアントと MAPI は、必要に応じてMAPI_TOP_LEVELをクリアするためにサービス プロバイダーに依存して、このフラグを初期化します。 
  
flags 値は、操作MAPI_TOP_LEVELの操作中に、この値に設定されます。 トップ レベル のオブジェクトは、操作を開始するためにクライアントによって呼び出されるオブジェクトです。 フォルダー コピー操作では、これがコピーされるフォルダーです。 フォルダーの削除操作では、削除するフォルダーです。 下位レベルのオブジェクトまたはサブオブジェクトを処理する呼び出しを行う場合は、フラグの値をクリアします。 フォルダー コピー操作では、サブオブジェクトは、コピーするフォルダー内のサブフォルダーです。 
  
MAPI を使用すると、MAPI_TOP_LEVEL フラグを使用して、トップ レベル のオブジェクトとサブオブジェクトを区別して、操作に関係するすべてのオブジェクトが同じ [IMAPIProgress](imapiprogressiunknown.md) 実装を使用して進行状況を表示でき、これによりインジケーター表示が 1 つの正方向にスムーズに進みます。 MAPI_TOP_LEVELフラグを設定するかどうかは、後続の progress オブジェクトの呼び出しで他のパラメーターの設定に影響します。 
  
複数レベルの操作のすべてのレベルで進行状況表示に適切なパラメーター値を設定する場合は、一部のサービス プロバイダーはサブオブジェクトの進行状況を表示しない選択を行う場合があります。 
  
 **サブオブジェクトの進行状況を表示しないようにするには**
  
- サブオブジェクトを処理する  _呼び出しで lpProgress_ パラメーターに NULL を渡します。 たとえば、フォルダーをコピーする場合は、サブフォルダーの [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) メソッドを呼び出します。 
    
- _lpProgress_ パラメーターの解釈方法を決定する特別なコードを記述します。 _lpProgress_ パラメーターの NULL 値は、MAPI 実装を使用してクライアントが進行状況を表示する必要があるという意味にもなりますので _、lpProgress_ パラメーターを無視する場合と [IMAPISupport::D oProgresDialog](imapisupport-doprogressdialog.md)を呼び出す場合を決定するには、特別なコードが必要です。
    
**IMAPIProgress::SetLimits** を呼び出して、MAPI_TOP_LEVEL フラグを設定またはクリアし、ローカルおよびグローバルの最小値と最大値を設定します。 フラグ設定の値は、進行状況オブジェクトがローカルまたはグローバルの最小値と最大値を理解するかどうかに影響します。 このフラグMAPI_TOP_LEVEL設定すると、これらの値はグローバルと見なされ、操作全体の進行状況を計算するために使用されます。 Progress オブジェクトは、グローバル最小値を 0 に、グローバル最大値を 1000 に初期化します。 
  
このMAPI_TOP_LEVEL設定されていない場合、最小値と最大値はローカルと見なされ、下位レベルのサブオブジェクトの進行状況を表示するためにプロバイダーによって内部的に使用されます。 Progress オブジェクトは **、GetMin** と **GetMax** が呼び出された場合にプロバイダーに返されるローカルの最小値と最大値のみを保存します。 
  
値、オブジェクト数、およびオブジェクトの合計パラメーターは **、IMAPIProgress::P rogress メソッドに入力** されます。 進行状況の割合を示す数値である value パラメーターが必要です。 このフラグMAPI_TOP_LEVEL設定されている場合は、オブジェクト数とオブジェクトの合計を渡す方法も指定できます。 一部のクライアントでは、これらの値を使用して、進行状況インジケーターを使用して "10 から 5 アイテムが完了しました" などの語句を表示します。 操作の進行状況は、パーセンテージとして、またはパーセンテージとして、および処理される合計から処理されたアイテムの数に関して厳密に報告できます。 たとえば、メッセージ ストア プロバイダーで、10 フォルダーをコピーするコピー操作を実行している場合、進行状況インジケーターは、操作が完了するまで、"1/10"、"10 の 2"、"3/ 10" などの語句を表示することで、ユーザーに追加情報を提供できます。 
  
## <a name="see-also"></a>関連項目



[MAPI 進行状況インジケーター](mapi-progress-indicators.md)

