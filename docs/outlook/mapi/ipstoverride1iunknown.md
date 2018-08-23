---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e73115811fe0009769826e0f6a011c489772f770
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569849"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
PSTDisableGrow ポリシーを無効にするには個人用フォルダー ファイル (PST) のストア プロバイダーを使用できます。
  
|||
|:-----|:-----|
|継承します。  <br/> |IUnknown  <br/> |
|によって実装されます。  <br/> |PST ストア プロバイダー  <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|インターフェイスの識別子。  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |個人用フォルダー (.pst) ファイルの登録の一覧を取得します。  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |HrTrustedPSTOverrideHandlerCallback それ以降の呼び出しを回避する自動ロック解除では、個人用フォルダー ファイルを登録します。  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |成長のための個人用フォルダー ファイルのロックを解除します。  <br/> |
   
## <a name="remarks"></a>注釈

PST をオーバーライドするハンドラーのインターフェイス識別子は可能性があります現在がある場合は、 [MAPI の定数](mapi-constants.md)のトピックで検索してコピーし、コードに追加のダウンロード可能なヘッダー ファイルで定義されていません。 値はシンボル名のグローバル一意識別子 (GUID) を関連付けるには、Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル guiddef.h に定義されている DEFINE_GUID マクロを使用します。 
  
詳細については、 [Outlook 2007 で PSTDisableGrow ポリシーをバイパスするのには、PST オーバーライドするハンドラーを実装する方法](http://support.microsoft.com/kb/956070)を参照してください。
  
## <a name="see-also"></a>関連項目



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

