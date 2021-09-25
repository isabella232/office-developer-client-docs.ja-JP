---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1f851d098819b583ab5a6e65b306e97ba01885e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587840"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用フォルダー ファイル (PST) ストア プロバイダーのリソースにアクセスします。
  
|||
|:-----|:-----|
|継承元:  <br/> |IUnknown  <br/> |
|実装元:  <br/> |PST ストア プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |個人用フォルダー (.pst) ファイルのロック解除手順を開始します。  <br/> |
   
## <a name="remarks"></a>注釈

PST オーバーライド ハンドラー インターフェイス識別子は、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は [、MAPI 定数](mapi-constants.md) のトピックで見つけ、それらをコピーしてコードに追加できます。 Microsoft Windows ソフトウェア開発キット (SDK) ヘッダー ファイル guiddef.h で定義されている DEFINE_GUID マクロを使用して、グローバル一意識別子 (GUID) 記号名をその値に関連付ける。 
  
詳細については、「PST オーバーライド[ハンドラーを実装して、2007 年の PSTDisableGrow](https://support.microsoft.com/kb/956070)ポリシーをバイパスするOutlook参照してください。
  
## <a name="see-also"></a>関連項目



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

