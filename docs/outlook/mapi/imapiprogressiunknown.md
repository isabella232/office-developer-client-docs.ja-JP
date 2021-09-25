---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5d5756aca0afdbad732b09b4dc79d8b7e4c08021
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625575"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
進行状況インジケーターをクライアント アプリケーションに提供する進行状況オブジェクトを実装します。 進行状況インジケーターは、メッセージ ストア間のフォルダーのコピーなど、操作の完了率を示すユーザー インターフェイス表示です。 MAPI およびクライアント アプリケーションは進行状況オブジェクトを実装し、サービス プロバイダーはそれらを使用します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |進行状況オブジェクト  <br/> |
|実装元:  <br/> |MAPI およびクライアント アプリケーション  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIProgress  <br/> |
|ポインターの種類:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[進行状況](imapiprogress-progress.md) <br/> |進行状況インジケーターを更新し、操作の完了に向けて進行状況を表示します。  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |進行状況の情報を計算する操作レベルの進行状況オブジェクトからフラグ設定を返します。  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |進行状況情報が表示される操作内のアイテムの最大数を返します。  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |進行状況情報が表示される [SetLimits](imapiprogress-setlimits.md) メソッドの最小値を返します。  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |操作のアイテム数の下限と上限、および操作の進行状況情報の計算方法を制御するフラグを設定します。  <br/> |
   
## <a name="remarks"></a>注釈

MAPI には、潜在的に長い操作を実行する多くのメソッドに  _lpProgress_ パラメーターが含まれています。  _lpProgress は_ 、進行状況オブジェクトのクライアント実装を示しています。 **IMAPIProgress インターフェイスを実装する** クライアントは、実装を指すこのパラメーターを設定します。**IMAPIProgress を実装しないクライアントは、** パラメーターを NULL に設定します。 操作の処理中に進行状況インジケーターを表示するには、サービス プロバイダーは、クライアントによって提供される進行状況オブジェクト (使用可能な場合)、または MAPI 実装  _(lpProgress が_ NULL に設定されている場合に示される) を使用します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**Files**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MapiProgress.h と MapiProgress.cpp  <br/> |該当なし  <br/> |IMAPIProgresss 設定が有効になっている場合、MFCMAPI は、実装を受け入れる MFCMAPI が呼び出すすべての関数に **IMAPIProgress** 実装を渡します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI のインターフェイス](mapi-interfaces.md)

