# # APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**material_document_year** | **string** |  |
**material_document** | **string** | Number of Material Document |
**material_document_item** | **string** |  |
**material** | **string** | Material Number | [optional]
**plant** | **string** |  | [optional]
**storage_location** | **string** |  | [optional]
**batch** | **string** | Batch Number | [optional]
**goods_movement_type** | **string** | Movement Type (Inventory Management) | [optional]
**inventory_stock_type** | **string** | Stock Type of Goods Movement (Stock Identifier) | [optional]
**inventory_valuation_type** | **string** |  | [optional]
**inventory_special_stock_type** | **string** |  | [optional]
**supplier** | **string** | Supplier&#39;s Account Number | [optional]
**customer** | **string** | Account number of customer | [optional]
**sales_order** | **string** | Sales Order Number | [optional]
**sales_order_item** | **string** |  | [optional]
**sales_order_schedule_line** | **string** |  | [optional]
**purchase_order** | **string** | Purchase Order Number | [optional]
**purchase_order_item** | **string** | Item Number of Purchasing Document | [optional]
**wbs_element** | **string** | Work Breakdown Structure Element (WBS Element) | [optional]
**manufacturing_order** | **string** |  | [optional]
**manufacturing_order_item** | **string** |  | [optional]
**goods_movement_ref_doc_type** | **string** | Goods movement ref doc type | [optional]
**goods_movement_reason_code** | **string** |  | [optional]
**delivery** | **string** |  | [optional]
**delivery_item** | **string** |  | [optional]
**account_assignment_category** | **string** |  | [optional]
**cost_center** | **string** |  | [optional]
**controlling_area** | **string** |  | [optional]
**cost_object** | **string** |  | [optional]
**gl_account** | **string** | G/L Account Number | [optional]
**functional_area** | **string** |  | [optional]
**profitability_segment** | **string** |  | [optional]
**profit_center** | **string** |  | [optional]
**master_fixed_asset** | **string** | Main Asset Number | [optional]
**fixed_asset** | **string** | Asset Subnumber | [optional]
**material_base_unit** | **string** |  | [optional]
**quantity_in_base_unit** | **float** |  | [optional]
**entry_unit** | **string** | Unit of entry | [optional]
**quantity_in_entry_unit** | **float** | Quantity in unit of entry | [optional]
**company_code_currency** | **string** |  | [optional]
**gds_mvt_ext_amt_in_co_code_crcy** | **float** | Externally Entered Posting Amount in Local Currency | [optional]
**sls_prc_amt_incl_vatin_co_code_crcy** | **float** | Value at Sales Prices Including Value-Added Tax | [optional]
**fiscal_year** | **string** |  | [optional]
**fiscal_year_period** | **string** | Period Year | [optional]
**fiscal_year_variant** | **string** |  | [optional]
**issg_or_rcvg_material** | **string** |  | [optional]
**issg_or_rcvg_batch** | **string** |  | [optional]
**issuing_or_receiving_plant** | **string** | Receiving/Issuing Plant | [optional]
**issuing_or_receiving_storage_loc** | **string** | Receiving/issuing storage location | [optional]
**issuing_or_receiving_stock_type** | **string** |  | [optional]
**issg_or_rcvg_spcl_stock_ind** | **string** |  | [optional]
**issuing_or_receiving_val_type** | **string** | Valuation Type of Transfer Batch | [optional]
**is_completely_delivered** | **bool** | \&quot;Delivery Completed\&quot; Indicator | [optional]
**material_document_item_text** | **string** | Item Text | [optional]
**goods_recipient_name** | **string** |  | [optional]
**unloading_point_name** | **string** |  | [optional]
**shelf_life_expiration_date** | **string** | Shelf Life Expiration or Best-Before Date | [optional]
**manufacture_date** | **string** |  | [optional]
**serial_numbers_are_created_automly** | **bool** | Create serial number automatically | [optional]
**reservation** | **string** | Number of reservation/dependent requirements | [optional]
**reservation_item** | **string** | Item Number of Reservation / Dependent Requirements | [optional]
**reservation_item_record_type** | **string** |  | [optional]
**reservation_is_finally_issued** | **bool** | Final Issue for Reservation | [optional]
**special_stock_idfg_sales_order** | **string** | Sales order number of valuated sales order stock | [optional]
**special_stock_idfg_sales_order_item** | **string** | Sales Order Item of Valuated Sales Order Stock | [optional]
**special_stock_idfg_wbs_element** | **string** | Work Breakdown Structure Element (WBS Element) | [optional]
**is_automatically_created** | **string** | Item Automatically Created Indicator | [optional]
**material_document_line** | **string** | Unique Identification of Document Line | [optional]
**material_document_parent_line** | **string** | Identifier of immediately superior line | [optional]
**hierarchy_node_level** | **string** | Hierarchy level of line in document | [optional]
**goods_movement_is_cancelled** | **bool** | Item has been Cancelled | [optional]
**reversed_material_document_year** | **string** | Reversed Material Document Year | [optional]
**reversed_material_document** | **string** | Reversed Material Document | [optional]
**reversed_material_document_item** | **string** | Reversed Material Document Item | [optional]
**reference_document_fiscal_year** | **string** | Fiscal Year of a Reference Document | [optional]
**invtry_mgmt_ref_document_item** | **string** | Item of a Reference Document | [optional]
**invtry_mgmt_reference_document** | **string** | Document No. of a Reference Document | [optional]
**material_document_posting_type** | **string** | Reversal, return delivery, or transfer posting | [optional]
**inventory_usability_code** | **string** |  | [optional]
**ewm_warehouse** | **string** | Warehouse Number/Warehouse Complex | [optional]
**ewm_storage_bin** | **string** |  | [optional]
**debit_credit_code** | **string** | Debit/Credit Indicator | [optional]
**to_material_document_header** | [**\BeLenka\SAP\MaterialDocument\Model\APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeCreate**](APIMATERIALDOCUMENTSRVAMaterialDocumentHeaderTypeCreate.md) |  | [optional]
**to_serial_numbers** | [**\BeLenka\SAP\MaterialDocument\Model\APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeCreateToSerialNumbers**](APIMATERIALDOCUMENTSRVAMaterialDocumentItemTypeCreateToSerialNumbers.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)