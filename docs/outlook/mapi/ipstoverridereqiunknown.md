---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389107"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーを格納する個人用フォルダー ファイル (PST) のリソースをアクセスします。
  
|||
|:-----|:-----|
|継承します。  <br/> |IUnknown  <br/> |
|実装元:  <br/> |PST ストア プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |個人用フォルダー (.pst) ファイルのロックを解除する手順を開始します。  <br/> |
   
## <a name="remarks"></a>備考

PST をオーバーライドするハンドラーのインターフェイス識別子は可能性があります現在がある場合は、 [MAPI の定数](mapi-constants.md)のトピックで検索してコピーし、コードに追加のダウンロード可能なヘッダー ファイルで定義されていません。 値はシンボル名のグローバル一意識別子 (GUID) を関連付けるには、Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル guiddef.h に定義されている DEFINE_GUID マクロを使用します。 
  
詳細については、 [Outlook 2007 で PSTDisableGrow ポリシーをバイパスするのには、PST オーバーライドするハンドラーを実装する方法](https://support.microsoft.com/kb/956070)を参照してください。
  
## <a name="see-also"></a>関連項目



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

