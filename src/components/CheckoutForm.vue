<template>
  <form class="row g-3 justify-content-center">
    <div class="col-md-5">
      <label for="first-name" class="form-label">First Name</label>
      <input type="text" class="form-control" id="first-name">
    </div>
    <div class="col-5">
      <label for="last-name" class="form-label">Last Name</label>
      <input type="text" class="form-control" id="inputAddress" placeholder="last-name">
    </div>
    <div class="col-10">
      <label for="Address" class="form-label">Address</label>
      <input type="text" class="form-control" id="Address" placeholder="Apartment, studio, or floor">
    </div>
    <div class="col-md-4">
      <label for="City" class="form-label">City</label>
      <input type="text" class="form-control" id="City">
    </div>
    <div class="col-md-2">
      <label for="inputState" class="form-label">State</label>
      <select id="inputState" class="form-select">
        <option selected>select state</option>
        <option value="AL">AL</option>
        <option value="AK">AK</option>
        <option value="AR">AR</option>
        <option value="AZ">AZ</option>
        <option value="CA">CA</option>
        <option value="CO">CO</option>
        <option value="CT">CT</option>
        <option value="DC">DC</option>
        <option value="DE">DE</option>
        <option value="FL">FL</option>
        <option value="GA">GA</option>
        <option value="HI">HI</option>
        <option value="IA">IA</option>
        <option value="ID">ID</option>
        <option value="IL">IL</option>
        <option value="IN">IN</option>
        <option value="KS">KS</option>
        <option value="KY">KY</option>
        <option value="LA">LA</option>
        <option value="MA">MA</option>
        <option value="MD">MD</option>
        <option value="ME">ME</option>
        <option value="MI">MI</option>
        <option value="MN">MN</option>
        <option value="MO">MO</option>
        <option value="MS">MS</option>
        <option value="MT">MT</option>
        <option value="NC">NC</option>
        <option value="NE">NE</option>
        <option value="NH">NH</option>
        <option value="NJ">NJ</option>
        <option value="NM">NM</option>
        <option value="NV">NV</option>
        <option value="NY">NY</option>
        <option value="ND">ND</option>
        <option value="OH">OH</option>
        <option value="OK">OK</option>
        <option value="OR">OR</option>
        <option value="PA">PA</option>
        <option value="RI">RI</option>
        <option value="SC">SC</option>
        <option value="SD">SD</option>
        <option value="TN">TN</option>
        <option value="TX">TX</option>
        <option value="UT">UT</option>
        <option value="VT">VT</option>
        <option value="VA">VA</option>
        <option value="WA">WA</option>
        <option value="WI">WI</option>
        <option value="WV">WV</option>
        <option value="WY">WY</option>
      </select>
    </div>
    <div class="col-md-4">
      <label for="Zip" class="form-label">Zipcode</label>
      <input type="text" class="form-control" id="Zip">
    </div>
    <div class="col-md-4">
      <label for="cardNum" class="form-label">Credit Card Number</label>
      <input type="text" class="form-control" id="cardNum">
    </div>
    <div class="col-md-2">
      <label for="cvv" class="form-label">CVV</label>
      <input type="text" class="form-control" id="cvv">
    </div>
<!--    <div class="col-md-4">-->
<!--      <label for="inputState" class="form-label">Expiration Date</label>-->
      <div class="col-md-2">
        <label for="inputState" class="form-label">Expiration date</label>
      <select id="inputState" class="form-select">
        <option selected>mm</option>
        <option>1</option>
        <option>2</option>
        <option>3</option>
        <option>4</option>
        <option>5</option>
        <option>6</option>
        <option>7</option>
        <option>8</option>
        <option>9</option>
        <option>10</option>
        <option>11</option>
        <option>12</option>
      </select>
      </div>
      <div class="col-md-2">
        <label for="inputState" class="form-label">(mm/dd)</label>
      <select id="inputState" class="form-select">
        <option>dd</option>
        <option>1</option>
        <option>2</option>
        <option>3</option>
        <option>4</option>
        <option>5</option>
        <option>6</option>
        <option>7</option>
        <option>8</option>
        <option>9</option>
        <option>10</option>
        <option>11</option>
        <option>12</option>
        <option>13</option>
        <option>14</option>
        <option>15</option>
        <option>16</option>
        <option>17</option>
        <option>18</option>
        <option>19</option>
        <option>20</option>
        <option>21</option>
        <option>22</option>
        <option>23</option>
        <option>24</option>
        <option>25</option>
        <option>26</option>
        <option>27</option>
        <option>28</option>
        <option>29</option>
        <option>30</option>
        <option>31</option>
      </select>
      </div>

    <div class="col-10">
      <div class="form-check">
        <input class="form-check-input" type="checkbox" id="gridCheck">
        <label class="form-check-label" for="gridCheck">
          Enable emails?
        </label>
      </div>
    </div>
    <div class="col-10">
      <button type="submit" class="btn btn-primary">Checkout</button>
    </div>
  </form>
</template>