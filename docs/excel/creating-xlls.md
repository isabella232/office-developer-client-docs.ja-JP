---
title: XLL を作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- dlls [excel 2007], calling into excel,xlAutoFree function [Excel 2007],xlAutoFree12 function [Excel 2007],xlcall32.lib [Excel 2007],xlAutoRegister function [Excel 2007],xlcall.cpp [Excel 2007],xlAutoRemove function [Excel 2007],xlAddInManagerInfo function [Excel 2007],xlAutoAdd function [Excel 2007],xlAutoOpen function [Excel 2007],xlAutoClose function [Excel 2007],DLLs [Excel 2007], turning into XLLs,XLLs [Excel 2007], calling into Excel,xlAutoRegister12 function [Excel 2007],xlcall.h [Excel 2007],xlAddInManagerInfo12 function [Excel 2007]
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 886b8e74f00f2e724785d43475ee0ffa3c922710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304145"
---
# <a name="creating-xlls"></a>XLL を作成する

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
DLL が自己完結型であるか、他のライブラリのみに依存する場合、Microsoft Excel を有効にしてその関数とコマンドにアクセスする方法について把握しておく必要があります。 詳細については、「[Excel で DLL にアクセスする](how-to-access-dlls-in-excel.md)」を参照してください。 
  
ただし、DLL が Excel の機能にアクセスする必要がある場合 (たとえば、セルの内容を取得するときや、ワークシート関数を呼び出すとき、または Excel を照会してワークスペース情報を取得するときなど) は、コードから Excel へのコールバックが可能でなければなりません。
  
Excel C API には、Dll が Excel にコールバックできるようにするいくつかの関数が用意されています。これらにアクセスするには、Excel 32 ビットライブラリ xlcall32 を使用して、コンパイル時に DLL を静的にリンクする必要があります。静的ライブラリは、このライブラリの 32 ビット版と 64 ビット版の両方を含む Microsoft Excel 2013 XLL SDK の一部として Microsoft からダウンロードできます。
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Dll から Excel へのコールバックを可能にする

DLL が Excel の機能にアクセスし、ワークスペース情報を取得または設定できるようにするには、まず Excel のコールバック関数 **Excel4**、**Excel4v**、**Excel12**、および **Excel12v** のアドレスを取得する必要があります。最後の 2 つは、Excel 2007 で導入され、以降のバージョンで利用可能です。これらのすべてにアクセスするには、DLL プロジェクトに、Excel 2013 XLL SDK から次のファイルへの参照が含まれている必要があります。最初の 2 つのコールバック (任意のバージョンの Excel) にのみアクセスする場合は、プロジェクトに最初の 2 つのファイルのみを含める必要があります。
  
### <a name="xlcallh"></a>Xlcall.h

Xlcall.h ファイルには、次の項目が含まれます。
  
- すべてのコールバック関数の関数プロトタイプ。
    
- DLL/XLL と ExcelDLL 間でのデータ交換にコールバックが使用するデータ構造の定義、データ型定数の定義。
    
- ワークシート関数、マクロ シート関数、およびサポートされている Excel コマンドに相当する C API 関数とコマンドの定義。
    
- コールバック関数の戻り値の定義。
    
このファイルでは、C API にアクセスするすべてのファイル、または C API が使用するデータ型を処理するすべてのファイルにおいて、このファイルの **#include** ディレクティブを (直接、あるいは別のヘッダー ファイルを介して間接的に) 使用する必要があります。 
  
### <a name="xlcall32lib"></a>Xlcall32.lib

Xlcall32 ライブラリは、最初の 2 つのコールバック、**Excel4** と **Excel4v**、および **XlCallVer** 関数もエクスポートします。プロジェクトでこのライブラリへの参照がなければ、コードでこれらのコールバックのいずれかを使用している場合は、リンカーは XLL を作成できません。(これらの関数のアドレスは、通常の Excel インストールの一部としてシステムにコピーされる同等の Xlcall32.dll に動的にリンクすることによって取得できます) 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

Excel のコールバック **Excel12** と **Excel12v** は Xlcall32.lib ではエクスポートされません。これにより、Excel 2007 以降で作成する XLL プロジェクトは、以前のバージョンの Excel でも機能します。Xlcall.cpp モジュールには **Excel12** および **Excel12v** 関数のコードが含まれており、Excel 2007 以降の Excel エントリ ポイントを呼び出したり、以前のバージョンの Excel を実行している場合は安全なエラー値を返したりします。Excel 2007 以降で実行する、より大きなグリッドと長い Unicode 文字列を処理する新しいデータ型を使用できる XLL を作成したい場合は、このモジュールをプロジェクトに含める必要があります。 
  
> [!NOTE]
> Excel 2010 SDK 以降では、このファイルは 32 ビットと 64 ビットの両方の XLL にコンパイルできます。 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>DLL を XLL に変換する: アドイン マネージャー インターフェイス関数

XLL は、Excel または Excel のアドイン マネージャーによって呼び出されるいくつかのプロシージャをエクスポートする DLL です。ここでは、これらのプロシージャを簡単に説明します。詳細な説明については、「[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)」を参照してください。これらの DLL コールバックはすべてプレフィックス **xlAuto** で始まります。これらのうち必須コマンドは **xlAutoOpen** のみです。これは、アドインが有効になると呼び出され、通常は Excel に XLL の関数とコマンドを登録してその他の初期化タスクを実行するために使用されます。すべての **xlAuto** 関数の関数シグネチャと実装例は、後のセクションで説明します。  
  
これらのコールバックの中で必須なのは **xlAutoOpen** だけですが、アドインの動作によっては、他のコマンドもエクスポートする必要がある可能性があります。 
  
Excel 2007 では、より大きなグリッドに対応し、長い Unicode 文字列をサポートするために、新しいデータ型 **XLOPER12** が導入されました。 **XLOPER12** については、このトピックの後半で説明します。**xlAuto** 関数は古いデータ型 **XLOPER** を取得または返すのに対し、これらの関数の新しいバージョンは **XLOPER12** データ型を使用する Excel 2007 で導入されました。**XLOPER12** のメモリリークを回避するために実装する必要がある **xlAutoFree12** を除いて、バージョン 12 の **xlAuto** 関数をすべて省略しても問題ありません (この場合、Excel 2007 以降では **XLOPER** バージョンが呼び出されます)。 
  
### <a name="xlautoopen"></a>xlAutoOpen

Excel は、XLL がアクティブになるたびに [xlAutoOpen](xlautoopen.md) 関数を呼び出します。正常終了した最後の Excel セッションでアクティブだったアドインは、次の Excel セッションの開始時にアクティブ化されます。アドインは、Excel セッション中に読み込まれると、アクティブになります。アドインが Excel セッション中に非アクティブにされてから再度アクティブにされる場合の、再アクティブ化のときにこの関数が呼び出されます。 
  
XLL の関数とコマンドの登録、データ構造の初期化、ユーザー インターフェイスのカスタマイズなどを行うには、**xlAutoOpen** を使用する必要があります。 
  
アドインが [xlAutoRegister](xlautoregister-xlautoregister12.md) 関数または [xlAutoRegister12](xlautoregister-xlautoregister12.md) 関数を実装してエクスポートする場合、Excel は最初に **xlAutoOpen** 関数を呼び出さずに関数やコマンドをアクティブ化して登録しようとすることがあります。この場合は、関数またはコマンドが正しく機能するように、アドインが十分に初期化されていることを確認する必要があります。そうなっていない場合、関数やコマンドの登録や、必要な初期化の実行が失敗します。 
  
### <a name="xlautoclose"></a>xlAutoClose

XLL ファイルが非アクティブになるたびに、Excel は [xlAutoClose](xlautoclose.md) を呼び出します。Excel セッションが正常に終了すると、アドインは非アクティブになります。Excel セッション中にユーザーがアドインを非アクティブ化する場合に、この関数は呼び出されます。 
  
関数とコマンドの登録解除、リソースの解放、カスタマイズの解除などを行うには、**xlAutoClose** を使用する必要があります。 
  
> [!NOTE]
> 関数とコマンドの登録解除に関しては、既知の問題があります。詳しくは、「[Excel XLL 開発での既知の問題](known-issues-in-excel-xll-development.md)」をご覧ください。 
  
### <a name="xlautoadd"></a>xlAutoAdd

ユーザーが Excel セッション中にアドイン マネージャーを使用して XLL をアクティブ化すると、Excel は [xlAutoAdd 関数](xlautoadd.md)を呼び出します。Excel が起動して、あらかじめインストールされたアドインを読み込む際には、この関数は呼び出されません。 
  
この関数を使用して、アドインがアクティブになっていることをユーザーに通知するカスタム ダイアログ ボックスの表示、レジストリに対する読み書き、またはライセンス情報の確認を行うことができます。
  
### <a name="xlautoremove"></a>xlAutoRemove

ユーザーが Excel セッション中にアドイン マネージャーを使用して XLL を非アクティブ化すると、Excel は [xlAutoRemove](xlautoremove.md) 関数を呼び出します。アドインがインストールされている状態で Excel セッションが終了するときには、正常終了でも異常終了でも、この関数は呼び出されません。 
  
この関数を使用して、アドインが非アクティブになっていることをユーザーに通知するカスタム ダイアログ ボックスを表示したり、レジストリへの読み書きを行うことができます。
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

アドイン マネージャーが Excel セッションで初めて呼び出されるとき、Excel は [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) 関数を呼び出します。Excel が 1 と等しい引数を渡す場合、この関数は文字列 (通常は、アドインの名前) を返す必要があります。それ以外の場合は、**#VALUE!** を返す必要があります。
  
Excel 2007 以降のバージョンでは、XLL によってエクスポートされる場合には **xlAddInManagerInfo** 関数ではなく **xlAddInManagerInfo12** 関数が呼び出されます。**xlAddInManagerInfo12** 関数は、**xlAddInManagerInfo** と同じように機能して、XLL の動作におけるバージョン固有の相違点を回避する必要があります。**xlAddInManagerInfo12** 関数は **XLOPER12** データ型を返し、**xlAddInManagerInfo** は **XLOPER** データ型を返す必要があります。 
  
### <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

Excel は登録対象の関数の戻り値の型と引数の型がない状態で、XLM 関数 **REGISTER**、または C API の同等の [xlfRegister](xlfregister-form-1.md) 関数に対する呼び出しが実行されると、常に [xlAutoRegister 関数](xlautoregister-xlautoregister12.md)を呼び出します。**xlAutoRegister**関数により、XLL はその内部にあるエクスポートされた関数とコマンドのリストを検索してその関数を引数とともに登録し、指定された型を返すことができます。 
  
Excel 2007 以降では、**xlAddInRegister12** 関数が XLL によってエクスポートされている場合、Excel はこの関数を **xlAddInRegister** 関数よりも優先して呼び出します。 
  
> [!NOTE]
> 引数と戻り値の型の指定がないままで **xlAddInRegister**/ **xlAddInRegister12** が関数を登録しようとすれば、再帰的な呼び出しのループが発生し、最終的にはコール スタックがオーバーフローして Excel が終了するか、応答しなくなります。 
  
### <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

Excel calls the [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md) function just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** data type with a flag set that tells Excel there is memory that the XLL still needs to release. This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks. Starting in Excel 2007, the **XLOPER12** data type is supported. For more information, see [Memory Management in Excel](memory-management-in-excel.md).
  
> [!NOTE]
> Starting in Excel 2007, when Excel is configured to use multithreaded worksheet recalculation, the **xlAutoFree**/ **xlAutoFree12** function is called on the same thread that was just used to call the function that returned it. The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread. This simplifies thread-safe design in your XLL. For more information, see [Multithreaded Recalculation in Excel](multithreaded-recalculation-in-excel.md). 
  
### <a name="creating-64-bit-xlls"></a>64 ビット XLL の作成

Excel およびユーザー定義関数は、32 ビット オペレーティング システムよりも優れたパフォーマンスを期待できる 64 ビット オペレーティング システムで実行可能です。Excel は、データの型に関する情報を含む **XLOPER12** 構造の値を渡します。**XLOPER12** 構造とネイティブ型 (**int** またはより大きい型に値を保持するポインターなど) の間で値を変換する場合はご注意ください。 
  
## <a name="see-also"></a>関連項目



[関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数を呼び出す](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)
  
[Excel XLL の開発](developing-excel-xlls.md)

