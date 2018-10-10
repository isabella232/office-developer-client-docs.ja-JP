---
title: Handler プロパティ (RDS)
TOCTitle: Handler Property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a020dfa5935cfe6a0b942c5234eda2a91c40d51
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477827"
---
# <a name="handler-property-rds"></a>Handler プロパティ (RDS)


**適用されます**Access 2013 |。Office 2013


[RDSServer.DataFactory](datafactory-object-rdsserver.md)のおよび*ハンドラー*によって使用されるパラメーターの機能を拡張するサーバー側のカスタマイズ プログラム (ハンドラー) の名前を示します。

## <a name="syntax"></a>構文

*DataControl*。ハンドラー =*文字列*

## <a name="parameters"></a>パラメーター

  - *DataControl*

  - [RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。

  - *String*

  - ハンドラーおよびパラメーターをすべてコンマ (たとえば、「handlerName、parm1、parm2、...、 *N*のパラメーター」) の名前を含む**文字列**値。

## <a name="remarks"></a>解説

このプロパティは、カスタマイズをサポートしますが、この機能を使用するには、[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定する必要があります。

ハンドラーの名前とパラメーターは、コンマ (",") で区切ります。*String* 内にセミコロン (";") が含まれていると、予期できない結果が発生する場合があります。また、**IDataFactoryHandler** インターフェイスをサポートしているハンドラーであれば、独自に作成することもできます。

既定のハンドラー名は **MSDFMAP.Handler** であり、この既定パラメーターは **MSDFMAP.INI** という名のカスタマイズ ファイルです。このプロパティは、サーバー管理者が作成した別のカスタマイズ ファイルを呼び出すときに使います。

[ConnectionString](connectionstring-property-ado.md)プロパティのハンドラーとパラメーターを指定するのには、**ハンドラー**のプロパティを設定する代わりに、"**ハンドラー =。 handlerName、parm1、parm2、...;*"です。

