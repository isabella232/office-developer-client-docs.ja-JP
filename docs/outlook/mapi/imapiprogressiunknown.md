---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 975c01457515a400d1d442fedc432dc000f06665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800651"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**適用対象**: Outlook 
  
進行状況インジケーターが表示されて、クライアント アプリケーションを提供する進行中のオブジェクトを実装します。 進行状況のインジケーターは、メッセージ ストア間でフォルダーをコピーするなど、操作の完了の割合が表示されるユーザー インターフェイスの表示です。 MAPI およびクライアント アプリケーションが実行中オブジェクトを実装し、サービス ・ プロバイダーを使用しています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |オブジェクトの進行状況  <br/> |
|によって実装されます。  <br/> |MAPI クライアント アプリケーション  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIProgress  <br/> |
|ポインターの型。  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |加えられると、操作の完了までの進捗状況の表示と進行状況のインジケーターが更新されます。  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |返します。 操作の進行状況に関する情報は、計算対象のレベルに進行中のオブジェクトから設定にフラグを設定します。  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |情報を表示する進行中の操作では、アイテムの最大数を返します。  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |進捗状況の情報が表示されます、 [SetLimits](imapiprogress-setlimits.md)メソッドでは、最小値を返します。  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |操作、および操作の進行状況の情報を計算する方法を制御するフラグでは、アイテム数の上限と下限の制限を設定します。  <br/> |
   
## <a name="remarks"></a>注釈

MAPI には、時間のかかる可能性のある操作を実行するメソッドの多くに、 _lpProgress_パラメーターが含まれています。  _lpProgress_は、実行中のオブジェクトのクライアントの実装を示しています。 **IMAPIProgress**インターフェイスを実装するクライアントは、それぞれの実装を指すには、このパラメーターを設定します。**IMAPIProgress**を実装していないクライアントは、パラメーターを NULL に設定されます。 操作の処理中に進行状況のインジケーターを表示するには、サービス プロバイダーは、可能な場合は、クライアントによって提供される進行中のオブジェクトまたは MAPI 実装では、( _lpProgress_は NULL に設定するときに示されます) を使用します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**ファイル**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MapiProgress.h と MapiProgress.cpp  <br/> |該当なし  <br/> |IMAPIProgress の設定を有効にすると、MFCMAPI 通過**IMAPIProgress**実装すべての関数 MFCMAPI を起動するに実装を受け入れることにします。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI インターフェイス](mapi-interfaces.md)

