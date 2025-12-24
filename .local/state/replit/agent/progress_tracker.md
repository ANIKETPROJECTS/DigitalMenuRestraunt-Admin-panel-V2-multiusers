[x] 1. Install the required packages
[x] 2. Restart the workflow to see if the project is working
[x] 3. Verify the project is working using the feedback tool
[x] 4. Inform user the import is completed and they can start building
[x] 5. Answered user question about image storage location and base64 implementation
[x] 6. Fixed image storage approach - base64 embedded directly in menu item:
    - Modified POST /api/admin/upload-image to return base64 string (not store separately)
    - Returns: { success, base64: "data:image/jpeg;base64,...", mimeType }
    - Frontend will save this base64 string directly in the item's image field
    - Result: Menu item document will have image: "data:image/jpeg;base64,..." (embedded base64)
    - Removed separate Image collection approach
[x] 7. Restarted workflow and verified server running successfully