---
title: Outlookソーシャル コネクタ プロバイダーのエラー コード
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: プロバイダーは、次の表に示すエラー コードのいずれかを使用して、呼び出し元にエラーを返す必要があります。
ms.openlocfilehash: 22a6e8d4ebf87157eaee630cc47f9f363150e839
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425352"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Outlookソーシャル コネクタ プロバイダーのエラー コード

プロバイダーは、次の表に示すエラー コードのいずれかを使用して、呼び出し元にエラーを返す必要があります。 
  
|**エラー**|**エラー コード (16 進数)**|**説明**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |ソーシャル ネットワーク サイトのネットワークで認証に失敗しました。  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |ソーシャル ネットワーク サイトへの接続に使用できる接続はありません。  <br/> |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |一般的なエラー エラー。  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |無効な操作が原因で内部エラーが発生しました。  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |関数に無効な引数が渡された。  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |前回の同期以降、変更は発生してこない。  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |リソースが見つかりません。  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |ソーシャル ネットワーク サイトへの要求は有効ですが、ソーシャル ネットワーク サイトによって実装されていません。  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |メモリ切れエラーが発生しました。  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |OSC プロバイダーは、リソースのアクセス許可を拒否しました。  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |ソーシャル ネットワーク アカウントを構成するサーバーのバージョンはサポートされていません。  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |プロバイダーは、このバージョンの OSC プロバイダーの機能拡張をサポートしていない。  <br/> |
   
## <a name="remarks"></a>注釈

成功、警告、およびエラーの値は、結果ハンドルまたは HRESULT と呼ばれる 32 ビット番号を使用 **して返されます**。 **HRESULT は** 何も処理しません。単なる 32 ビット値で、複数のフィールドが値にエンコードされています。 正の結果は、状態の成功を示し、0 の結果は状態 (S_OK) のない成功を示し、負の結果は失敗を示します。 
  

