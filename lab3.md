# codelab3
<div class="container">
    <h2>Product Details</h2>
    <form [formGroup] = "prodForm" action="">
        <div class="form-group" >
            <label class="form-check-label">Product Id </label>
            <input type="text" style="display: inline-block; width: 40%; margin-left: 55px; " formControlName="productId" class="form-control"  [class.is-invalid]="prodForm.get('productId').invalid && prodForm.get('productId').touched">
            <small [class.d-none]="prodForm.get('productId').valid || prodForm.get('productId').untouched" class="text-danger">Product Id is mandatory.</small>
        </div>

        <div class="form-group">
            <label>Product Name</label>
            <input type="text" style="display: inline-block; width: 40%; margin-left: 27px;" formControlName="productName" class="form-control" [class.is-invalid]="prodForm.get('productName').invalid && prodForm.get('productName').touched">
            <small [class.d-none]="prodForm.get('productName').valid || prodForm.get('productName').untouched" class="text-danger">Product Name is mandatory.</small>
        </div>

        <div class="form-group">
            <label>Product Cost</label>
            <input type="text" style="display: inline-block; width: 40%; margin-left: 35px;" formControlName="productCost" class="form-control" [class.is-invalid]="prodForm.get('productCost').invalid && prodForm.get('productCost').touched">
            <small [class.d-none]="prodForm.get('productCost').valid || prodForm.get('productCost').untouched" class="text-danger">Product Cost is mandatory.</small>
        </div>

        <div class="form-group">
            <label>Product Online</label>
            <div class="form-check" style="display: inline-block; margin-left: 30px;">
                <input class="form-check-input" type="radio" formControlName="productOnline" value="yes" [class.is-invalid]="prodForm.get('productOnline').invalid && prodForm.get('productOnline').touched">
                <label class="form-check-label">Yes</label>
            </div>
            <div class="form-check" style="display: inline-block; margin-left: 30px;">
                <input class="form-check-input" type="radio" formControlName="productOnline" value="no" [class.is-invalid]="prodForm.get('productOnline').invalid && prodForm.get('productOnline').touched">
                <label class="form-check-label">No</label>
            </div>
        </div>

        <div class="form-group">
            <label>Choose Category</label>
            <select class="custom-select" style="display: inline-block; width: 40%; margin-left: 5px; " formControlName="productCategory" [class.is-invalid]="prodForm.get('productCategory').invalid && prodForm.get('productCategory').touched">
                <small [class.d-none]="prodForm.get('productCategory').valid || prodForm.get('productCategory').untouched" class="text-danger">Product Category is mandatory.</small>
                <option>Select Category</option>
                <option *ngFor="let category of categories">{{category}}</option>
            </select>
        </div>

        <div class="form-group" >
            <label>Availability in store</label>
            <div class="form-check" style="display: inline-block; margin-left: 20px;">
                <input class="form-check-input" type="checkbox" formControlName="productAvail">
                <label class="form-check-label">Big Bazar</label>
            </div>
            <div class="form-check" style="display: inline-block; margin-left: 20px;">
                <input class="form-check-input" type="checkbox" formControlName="productAvail">
                <label class="form-check-label">D Mart</label>
            </div>
            <div class="form-check" style="display: inline-block; margin-left: 20px;">
                <input class="form-check-input" type="checkbox" formControlName="productAvail">
                <label class="form-check-label">Reliance</label>
            </div>
            <div class="form-check" style="display: inline-block; margin-left: 20px;">
                <input class="form-check-input" type="checkbox" formControlName="productAvail">
                <label class="form-check-label">Mega Store</label>
            </div>
        </div>

        <button class="btn btn-primary" type="submit" (click)="onClick()">Add Product</button>
    </form>
    
</div>


#code lab4
